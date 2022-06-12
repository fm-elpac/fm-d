# FMRW-1
胖蚊子重写

快速重写任意软件的 AI 系统


## 主要设计

+ 主要技术: NLP, 神经网络, 虚拟机, 编译器

+ 主要思想: 分层抽象, 系统论, 抽象+细节

+ 抽象训练过程: 公共模式提取, 模式命名

+ 迭代式训练:

  第 0 代: 没有学习到的知识, 只有先验知识

  第 1 代: 加入第 0 代学习到的知识, 重构系统

  .. .

  每一代的语言是冻结的, 新一代使用新一代语言.

+ 系统抽象语言: 抽象+细节

+ 非直接修改, 高抽象编程 ?

### 抽象语言层级

+ [计算机语言域] 特定低级语言抽象层级

  机器语言/汇编语言

+ [计算机语言域] 通用低级语言抽象层级

+ [计算机语言域] 特定高级语言抽象层级

+ [计算机语言域] 通用高级语言抽象层级

+ [核心抽象语言] 架构语言抽象层级

+ [人类语言域] 通用人类语言抽象层级

+ [人类语言域] 特定人类语言抽象层级


TODO