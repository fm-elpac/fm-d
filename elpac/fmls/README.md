# FMLS
胖蚊子轻蜘蛛 (Fat Mosquito Light Spider)

设备互连与资源共享.


## 主要功能模块

+ 设备聊天

  设备身份 (公钥), 设备发现与连接 (比如扫描二维码), 设备分组, 抽象设备

  设备消息发送 (聊天), 多通道聊天 (channel),
  安全信道 (HTTP/2, HTTP/3, ssh), 端到端加密

  设备资源共享 (安全组), 剪切板共享, 文件共享 (sshfs),
  IO 设备共享 (设备合并)

  基于 `娲刺` 的高级设备合并功能 ?

+ 控制中心

  比如 PMLZ-1 胖喵小窝, FMRF-1 胖蚊子兔场 等的设备遥控

  PMUV-2 胖喵紫外线强度计 (蓝牙 BLE)

+ 远程设备

  - 远程手机 (操作端 和 被控端)

  - 远程桌面


## 主要代码仓库

+ `fmls-server` 服务器端 (树莓派, 机架服务器, OpenWRT 路由器)

  rust (risc-v, arm, x86), GNU/Linux

+ `fmls-apk` Android 设备 (手机, 平板)

  Android 8.1+ (flutter), fuchsia ?

  package: `org.fm_elpac.fmls.apk`

+ `fmls-dt` 桌面设备 (台式机/笔记本)

  GNU/Linux, Windows (electron ?)


## 基于的技术

### 局域网 设备发现和互连技术

+ **`mDNS` / `DNS-SD`**

  可用于服务发现: 比如多个设备上安装了同一个 app, app 向系统注册,
  那么一个设备就能发现别的设备上运行的相同 app.

  支持 Android (`NsdManager`), GNU/Linux (`avahi`),
  以及 Windows/苹果 (`dns-sd`).

  ----

  FMLS 计划使用的服务类型: `uuid#*._fmls1_http2._tcp.local`

  附加数据:
  `pk=sha256:*`

+ **路由器将 `hostname` 加入 `DNS`**

  可以实现 ping 主机名时, 自动解析为对应设备的 IP 地址 (动态分配 IP).

  有的路由器不支持, 可以考虑换成 OpenWRT 路由器 (确认支持).

+ **蓝牙**

  Android 的蓝牙功能, 支持两只手机上的 app 直接交换数据 (p2p 方式).

+ **Wifi Direct** (WLAN 直连)

  无需 wifi 路由器, 直接通过 wifi 连接两只设备.

  支持 Android (`WifiP2pManager`) 等.

### 广域网 设备互连技术

+ **`IPv6` + `DDNS`**

  具有 IPv6 的设备 (家用宽带, 手机 4G/5G 目前基本都支持分配 IPv6 地址),
  一般都具有公网地址 (`2408:*`), 可直接互连.

  DDNS (Dynamic DNS) 有很多免费的, 通过动态更新设备 IP 地址,
  当设备的 IP 地址变动后, 也能通过固定域名正确解析.

  综上, IPv6 + DDNS 成本很低, 几乎可以免费使用.

  TODO 推荐的免费 DDNS 网站

+ **通过云端服务器中转**

  比如在 腾讯云, 阿里云 等买一台云服务器, 然后部署相关软件.

  这种方式需要付费, 而且还不便宜.

### 设备通信协议

大部分是 web 平台的技术, 优点包括 标准开放,
跨平台, 使用广泛, 生态丰富, 使用方便 等.

+ **`ssh`** (以及 `sshfs`)

  较高的安全性, 公钥加密, 免密码认证.

  丰富的功能: 远程登录执行命令, 文件共享 (sftp, sshfs)， 端口转发 等.

  较高的性能.

+ **`HTTP/2`, `HTTP/3` (`QUIC`)**

  强制加密, 使用广泛.

  C/S 模式的协议, 具有丰富的功能.

+ **`WebSocket`**

  可选加密, 基于 HTTP/1.1

  C/S 模式全双工消息协议.

  目前主要优点是支持广泛, 比较成熟.
  未来可能被 WebTransport 取代.

+ **`WebRTC`**

  强制加密 (DTLS), 自带内网穿透 (STUN/TURN, ICE).

  p2p 模式的强大实时通讯协议.
  具有实时视频/音频通信 (SRTP), 流量控制 (自适应码率),
  实时数据发送 (DataChannel, SCTP) 等功能.

  可用于 视频通话, 视频会议, 直播, 云游戏, 远程桌面 等.

+ **`WebTransport`**

  强制加密, 基于 HTTP/3 (QUIC).

  C/S 模式的强大协议.
  功能上可取代 WebSocket 和 WebRTC (部分, 配合 WebCodec, WASM 等).

  目前处于草案阶段, Chrome 浏览器可用.


TODO
