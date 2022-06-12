# FM3P
胖蚊子系列 3D 打印机


## 主要计划

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
    <th>打印材料 <br /> : 次要材料</th>
    <th>打印范围</th>
    <th>驱动方式</th>
    <th>备注</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="2">FM3P-1</td>
    <td>中型三角洲打印机</td>
    <td>熔融沉积 (常温 FDM)</td>
    <td>高 100cm, 底边 40cm, 碳杆 30cm <br /> (亚克力透明外壳)</td>
    <td>0.2mm (0.1mm)</td>
    <td>~1000 ?</td>
  </tr>
  <tr>
    <td>三角洲 (delta)</td>
    <td>塑料/橡胶 (PLA, ABS, PETG, TPU) <br /> : 泥土 (陶瓷), 水泥, 面粉 (食物) 等</td>
    <td>圆柱形, 直径 280mm, 高 400mm</td>
    <td>步进电机 (开环), 光轴 (直线轴承), 丝杆</td>
    <td>基于 Kossel (1.66x)</td>
  </tr>

  <tr>
    <td rowspan="2">FM3P-2</td>
    <td>大型三角洲打印机</td>
    <td>熔融沉积 (常温 FDM)</td>
    <td>高 200cm, 底边 80cm, 碳杆 60cm <br /> (开放式无外壳)</td>
    <td>0.5mm (0.2mm)</td>
    <td></td>
  </tr>
  <tr>
    <td>三角洲 (delta)</td>
    <td>塑料/橡胶 (PLA, PETG), 水泥, 泥土 (陶瓷) 等</td>
    <td>圆柱形, 直径 50cm, 高 80cm</td>
    <td>伺服电机 (闭环), 齿条导轨 <br /> (FPGA)</td>
    <td></td>
  </tr>

  <tr>
    <td rowspan="2">FM3P-3</td>
    <td>小型高精度三角洲打印机</td>
    <td>熔融沉积 (常温 FDM)</td>
    <td>高 50cm, 底边 20cm, 碳杆 15cm <br /> (亚克力透明外壳)</td>
    <td>< 0.1mm (0.05mm)</td>
    <td></td>
  </tr>
  <tr>
    <td>三角洲 (delta)</td>
    <td>塑料/橡胶 (PLA, ABS, PETG, TPU) <br /> : 泥土 (陶瓷)</td>
    <td>圆柱形, 直径 140mm, 高 200mm</td>
    <td>步进电机 (闭环), 光轴 (直线轴承), 丝杆 <br /> (FPGA)</td>
    <td></td>
  </tr>

  <tr>
    <td rowspan="2">FM3P-4</td>
    <td>无限 Z 轴塑料打印机</td>
    <td>熔融沉积 (常温 FDM)</td>
    <td></td>
    <td>0.2mm (0.1mm)</td>
    <td></td>
  </tr>
  <tr>
    <td>CoreXY (无限 Z 轴)</td>
    <td>塑料/橡胶 (PLA, PETG)</td>
    <td></td>
    <td>步进电机 (开环), 光轴 (直线轴承), 同步带</td>
    <td></td>
  </tr>

  <tr>
    <td rowspan="2">FM3P-5</td>
    <td>低成本机械臂塑料打印机</td>
    <td>熔融沉积 (常温 FDM)</td>
    <td></td>
    <td>0.2mm (0.1mm)</td>
    <td>< 500 ?</td>
  </tr>
  <tr>
    <td>机械臂 (SCARA)</td>
    <td>塑料/橡胶 (PLA, ABS, PETG, TPU) <br /> : 泥土 (陶瓷), 水泥, 面粉 (食物) 等</td>
    <td></td>
    <td>步进电机 (开环), 齿轮, 同步带 等</td>
    <td>基于 RepRap Morgan</td>
  </tr>

  <tr>
    <td rowspan="2">FM3P-6</td>
    <td>食物打印机</td>
    <td>黏着沉积 (常温)</td>
    <td></td>
    <td>2mm (1mm)</td>
    <td>< 1000 ?</td>
  </tr>
  <tr>
    <td>机械臂 (SCARA)</td>
    <td>水, 糊状食材, 粉状食材, 颗粒食材 等</td>
    <td>直径 30cm, 高 10cm</td>
    <td></td>
    <td></td>
  </tr>

  <tr>
    <td rowspan="2">FM3P-10</td>
    <td>胖蚊子毛线编织机</td>
    <td>针织纬编</td>
    <td></td>
    <td>2mm (1mm)</td>
    <td></td>
  </tr>
  <tr>
    <td>针织横机</td>
    <td>毛线</td>
    <td>宽 100cm, 长无限制</td>
    <td></td>
    <td>基于 OpenKnit</td>
  </tr>

  <tr>
    <td rowspan="2">FM3P-11</td>
    <td>胖蚊子细线编织机</td>
    <td>针织纬编</td>
    <td></td>
    <td>0.5mm (0.2mm)</td>
    <td></td>
  </tr>
  <tr>
    <td>针织横机</td>
    <td>棉线 等</td>
    <td>宽 80cm, 长无限制</td>
    <td> (FPGA)</td>
    <td></td>
  </tr>

  <tr>
    <td rowspan="2">FM3P-20</td>
    <td>胖蚊子高温打印机 (1300 K)</td>
    <td>熔融沉积 (高温 FDM)</td>
    <td></td>
    <td>0.2mm (0.1mm)</td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td>玻璃</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>

  <tr>
    <td rowspan="2">FM3P-21</td>
    <td>胖蚊子超高温打印机 (2000 K)</td>
    <td>熔融沉积 (高温 FDM)</td>
    <td></td>
    <td>0.2mm (0.1mm)</td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td>不锈钢 等金属</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>

  <tr>
    <td rowspan="2">FM3P-22</td>
    <td>胖蚊子冰打印机 (< 270K)</td>
    <td>熔融沉积 (低温 FDM)</td>
    <td></td>
    <td>0.2mm (0.1mm)</td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td>水 (冰) 等液体</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>

  <tr>
    <td rowspan="2">FM3P-30</td>
    <td>胖蚊子化妆机</td>
    <td>黏着沉积 (常温, 曲面 3D)</td>
    <td>约 50x50x100cm (前面板 50x50cm, 工作区域)</td>
    <td>0.2mm (0.1mm)</td>
    <td>< 10_000</td>
  </tr>
  <tr>
    <td>多机械臂 (8)</td>
    <td>液体, 粉状固体 等化妆品</td>
    <td>人脸 (30x30x15cm)</td>
    <td> (FPGA)</td>
    <td></td>
  </tr>

  <tr>
    <td rowspan="2">FM3P-31</td>
    <td>胖蚊子便携化妆机</td>
    <td>黏着沉积 (常温, 曲面 3D)</td>
    <td>20x40x10cm (收起)</td>
    <td>0.2mm (0.1mm)</td>
    <td>< 20_000</td>
  </tr>
  <tr>
    <td>多机械臂 (4)</td>
    <td>液体, 粉状固体 等化妆品</td>
    <td>人脸 (25x25x10cm)</td>
    <td> (FPGA)</td>
    <td></td>
  </tr>

</tbody>
</table>

注*: 成本仅供参考.


## 常见特性

+ 硬件冗余安全防护 (急停按钮)

+ 精简界面: 状态指示灯与压电陶瓷蜂鸣器

+ 断料检测与保护

+ 温度检测与保护

+ (可选) 封闭外壳与通风系统

+ (可选) 自动调平

+ (可选) 热床 (超声波热床 ?)

+ USB (2.0) 上位机 (比如 树莓派)

+ 手机 (Android) 上位机 (FMPR) (BLE/wifi, esp32c3)

+ (可选) SD 卡与脱机运行 (无上位机)


## 设计参考

+ RepRap <https://www.reprap.org/>

  - Kossel <https://reprap.org/wiki/Kossel>

  - Morgan <https://reprap.org/wiki/RepRap_Morgan>

+ OpenKnit <https://github.com/g3rard/OpenKnit>

+ 固件 <https://reprap.org/wiki/List_of_Firmware>

  - Klipper <https://github.com/KevinOConnor/klipper>

  - Marlin <https://marlinfw.org/>


TODO
