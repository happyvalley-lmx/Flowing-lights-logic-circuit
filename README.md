# Flowing-lights-logic-circuit

依靠逻辑电路芯片实现的流水灯
![Main_Board](https://raw.githubusercontent.com/happyvalley-lmx/Flowing-lights-logic-circuit/main/pic/main_board.jpg)

## 简介

### 功能:

实现三种不同的流水方案。

可以手动调节流水速度。

### 原理:

采用 **CD4017** 计数器输出端接发光二极管实现流水效果。

通过 **NE555** 在无稳态工作输出方波产生计数信号，通过电位器改变阻值实现改变频率，从而改变整体系统流水速度。

使用 **74LS32** 或门配合 **CD4017** 实现单按键选择流水方案。

## 实现

采用 **Altium Designer** 进行原理图与PCB的绘制。

BOM单如下

| Part                       | Qty  |
| -------------------------- | ---- |
| 2.2kΩ  AXIAL-0.4 Resistor  | 1    |
| 10kΩ  AXIAL-0.4 Resistor   | 2    |
| 1kΩ  AXIAL-0.4 Resistor    | 10   |
| CD4017BE                   | 3    |
| NE555P                     | 1    |
| 74LS32P                    | 1    |
| LED_3MM                    | 10   |
| 50kΩ 3296W Potentiometer   | 1    |
| 1uF Electrolytic Capacitor | 1    |
| 0.1uF Ceramic Capacitors   | 1    |
| 6*6 key                    | 1    |

### 使用说明：

**输入电压/工作电压:** 5V

**按键功能:** 切换三种流水方式与待机。切换顺序为：正序流水→逆序流水→双向流水→待机→正序流水→...

首次上电时，有大概率处于无效待机态，须多按几次按键进入正常循环切换状态。
