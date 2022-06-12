# ASFS
阴影文件系统 (Android Shadow File System)

+ rust, fuse

+ sqlite

+ magisk

+ sshfs

应用数据 (`/data/data`, `/sdcard/Android`) 存储在服务器上,
本地只是一个缓存.

通过 sshfs 访问服务器的文件, 可以使用任意支持 ssh 的服务器.
Android 挂载 sshfs (fuse) 需要 root.

asfs 实现一个本地缓存.
一级缓存位于手机内置存储 (`/data/data`).
二级缓存 (可选) 位于 SD 卡 (如果手机有 SD 卡槽).

asfs 通过 fuse 挂载到应用数据目录 (比如 `/data/data`).
当应用访问数据文件时, asfs 首先查找缓存, 如果缓存命中则直接访问.
否则通过 sshfs 访问服务器的数据.

本地缓存用于提高应用读写数据文件的性能,
同时减少通过网络访问服务器的流量.
本地缓存可设置大小, 比如 10GB, 多个应用可共享缓存空间.
缓存默认策略是 LRU (当缓存满时, 清除最近没有访问的数据).

asfs 实现的效果 (理想) 是, 将手机存储扩大为服务器容量 (比如 2TB).
同时应用读写数据文件的性能只有小幅度下降.

比如: 在存储只有 32GB 的手机上, 使用 asfs 可以允许 QQ 占用 60GB 存储空间.

----

asfs (magisk module)

asfs (rust)

asfs --daemon --config 配置管理器

asfs --cached --meta 缓存管理器

asfs --logd 文件访问日志

asfs --mount 具体 FUSE 工作进程

asfs-ai 使用 AI 预测 app 的文件访问, 用于预取等提高性能


TODO
