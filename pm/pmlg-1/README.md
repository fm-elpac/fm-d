# PMLG-1
胖喵学习游戏


## 主要设计

+ 学习游戏: 以 3D VR 交互式游戏作为学习材料的展现形式.

  学习材料的发展趋势:

  1. 图文 (传统: 文字+图片)
  2. 视频 (音频)
  3. 3D VR 交互式游戏 (PMLG-1)

  重点是使用游戏的相关技术, 而不局限于现有游戏的具体形式.

+ 以 git 数据库进行去中心化分布式的数据存储 (类似 web 网页).

+ 客户端: 学习浏览器

  是内容的浏览器, 也是编辑器.
  用户在浏览已有内容的同时, 也能创作新的内容.

  集成内置 web 浏览器 (chromium/firefox).

  支持多种硬件级别 (HL).


## git 数据库
类似 web 的内容发布方式.

+ 基本原则: 数据存储提供高度灵活性.
  去中心化分布式设计.

  对较差的网络提供良好支持.
  (低速/不稳定)

+ 多分支设计: 数据分散在多个 git 分支上,
  减少拉取数据时的流量.

+ 支持单个/多个 git 仓库, 公开/私有 git 仓库:
  各个数据分支可以全部位于一个 git 仓库中,
  也可以分散在多个 git 仓库.

  镜像分支: 可以镜像别的 git 仓库的内容.

  支持仓库数据的拆分/合并/转移, 多仓库容量管理.

+ 使用 URL 标记 git 仓库, 一个人/群组对应一个主仓库.

  一个人的仓库, 包括以下数据:

  - 个人信息: 昵称, 联系方式, GPG 公钥 等.

  - 关注列表: 指向别的人/群组的主仓库 (URL).

  - 内容列表: 本仓库发布的内容.

  - 内容项目: 每个内容项目相当于一个网页 (学习游戏).

  群组的仓库, 包括以下数据:

  - 成员列表: 指向别的人/群组的主仓库 (URL).

+ 支持多种平台, 内容可在任意网站发布, 只要支持 git 即可.

+ 上游 (upstream) git 仓库:

  用于更新客户端.
  包含版本号, 下载地址, 配置数据等.


## 硬件级别

+ `HL0` 浏览器级 (2D 屏幕+鼠标键盘)

  作为 web 应用直接在浏览器中运行, 无需安装.

  适用于笔记本/台式机.

+ `HL1` app 级 (2D 触摸屏幕)

  下载安装 apk.

  适用于 Android 手机/平板.

+ `HL2` 手机 VR 级 (3D VR)

  手机 + 几十元的塑料 VR 盒子.

  最便宜的 VR 方案, 效果较差.

+ `HL3` 头戴 VR 级 (3D VR)

  专用头戴 VR 设备, 价格约 2000 元 ~ 2 万元.

  效果较好的 VR, 支持复杂的 VR 交互.

+ `HL4` 遥铠级 (3D VR + 力反馈支架)

  HL3 级别的 VR 设备 + 遥铠驾驶舱 (力反馈支架).

  可以使用 FMRA-1 胖蚊子遥铠 (标准版) 的驾驶舱,
  也可以使用 FMRA-2 胖蚊子遥铠轻量版 的简易设备.

  具有目前最佳的 VR 交互效果, 比如可以 "触摸" VR 物体.

+ `HL5` (保留) 超高级


## 学习浏览器

主要模块:

+ `data` 去中心化分布式数据存储 (git)

+ `ext` 插件扩展系统: WASM, wasmer

+ `im` 集成聊天模块 (插件扩展)

+ `browser` 集成 web 浏览器 (chromium/firefox)

+ `ui` 用户界面

  - 2D 界面 (HL0, HL1)

  - 3D VR 界面 (HL2, HL3)

  - 遥铠界面 (HL4)

  - 语音界面 (she-os)

+ `game` 游戏引擎: 主要内容呈现

+ `ed` 内容创作编辑器 (blender ?)

安装包:

+ `pmlg.apk` 学习浏览器 主安装包

+ `pmlg_web.apk` 集成 web 浏览器

+ `pmlg_ed.apk` 内容创作编辑器


## 学习游戏的主要形式

+ 动态模型演示 (物理引擎)

+ 操作练习环境 (模拟)

应该注重培养计算机/机器没有的能力, 从而保持作为人的优势.
计算机在旁边随时辅助.


TODO
