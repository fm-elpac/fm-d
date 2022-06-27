# PMLC-1
胖喵小云

组建微型云计算系统的技术方案.


## 硬件

二手机架服务器.

典型配置:

+ 规模: 2U 双路

+ 内存: 64GB DDR4

+ 存储:

  - 系统盘: 480GB (SSD 480GB x2) RAID-1

    btrfs

  - 数据盘 (磁盘阵列): 9TB (3TB x4) RAID-5

    LVM, swap

  - 数据盘 (非阵列): 12TB (3TB x4)

    LVM

+ 网络: 千兆/万兆以太网 (1Gbps, 10Gbps)


## 基础软件

+ 物理机操作系统: Debian 11

+ 虚拟机: KVM/qemu, libvirt

+ 基础设施层 (IaaS): openstack (虚拟机)

+ 平台层 (PaaS): k8s (容器)


## 应用软件

(SaaS)

+ gitlab-ce

+ fmls-server 胖蚊子轻蜘蛛 (服务端)

+ pmeh-server 胖喵吃多少 (服务端)

+ pmlh-server 胖喵 AI 小助手 (服务端)


TODO
