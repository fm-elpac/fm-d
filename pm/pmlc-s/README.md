# PMLC-S
胖喵小云集群管理软件

+ 编程语言: rust

+ 替代: openstack

+ 适用于: 2 ~ 16 台物理服务器

+ 支持操作系统: Debian 11

+ 主要目标:

  - 保持物理机干净

  - 降低系统复杂度

  - 减小攻击面


## 依赖

+ kvm/qemu, libvirt

+ systemd

+ openssh

+ git


## 主要组件

+ `pmlc-s` 系统级管理操作 (root)

+ `pmlc-m` 监视: 日志收集和生成

+ `pmlc-v` 虚拟机 (计算资源) 管理

+ `pmlc-d` 存储资源管理

+ `pmlc-n` 网络资源管理 (SDN)


## 安全

+ 使用 SELinux 严格限制各个组件的行为

+ rust: 禁止使用 unsafe

+ 高可用 (HA): 任意单个服务器故障, 不会导致集群整体故障

+ 用户角色: (权限)

  - 管理员

  - 观察者

  - 普通用户

+ 异地灾备


TODO
