# FM3P-1
胖蚊子 3D 打印机: 中型并连臂


<table>
<thead>
  <tr>
    <th rowspan="2">代号</th>
    <th>描述</th>
    <th>成形技术</th>
    <th>框架大小</th>
    <th>精度 (理想精度)</th>
    <th>成本 (CNY) *</th>
  </tr>
  <tr>
    <th>结构类型</th>
    <th>打印材料</th>
    <th>打印范围</th>
    <th>驱动方式</th>
    <th>备注</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="2">FM3P-1</td>
    <td>中型并连臂</td>
    <td>熔融沉积 (常温 FDM)</td>
    <td>高 100cm, 底边 40cm, 碳杆 30cm <br /> (亚克力透明外壳)</td>
    <td>0.1mm (50um)</td>
    <td>~1000 ?</td>
  </tr>
  <tr>
    <td>三角洲 (delta)</td>
    <td>塑料 (橡胶)</td>
    <td>圆柱形, 直径 280mm, 高 400mm</td>
    <td>FMMC 无刷电机, 光轴 (直线轴承), 丝杆</td>
    <td>基于 Kossel (1.66x)</td>
  </tr>
</tbody>
</table>

注*: 成本仅供参考.


## 主要设计

+ 驱动方式: FMMC 无刷电机 + 丝杆

+ 主控制器: FMMC FPGA 运动控制板

+ 辅助控制器: `ch32v103`

  MCU 上位机 (SD 卡, 电池供电)

  脱机打印, 断电续打

+ 机器最高工作温度 (环境): 50 摄氏度

+ 结构组件:

  - 框架: 铝型材
  - 外壳: 亚克力板
  - 悬杆: 碳杆, 关节轴承

+ 自动调平: 力反馈调平

+ 高速打印


TODO
