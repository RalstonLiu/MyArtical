
# Maixduino AI 开发板 众测来袭

![](https://mc.dfrobot.com.cn/data/attachment/forum/202006/10/155848pjxnxsrs1k4scnkq.jpg)

### 什么是 Maixduino？
Maixduino是一款基于Kendryte K210 RISC-V AI处理器、基于Arduino UNO形式并且板载ESP32 Wi-Fi 和蓝牙模块以及M1 AI模块的AI开发板。
让 Maix 系列的开发板（k210 芯片）支持 Arduino IDE及库， 方便使用大量已有的开源 Arduino 库， 从而快速进行开发和原型验证。

产品链接：[点击查看](https://www.dfrobot.com.cn/goods-2592.html "点击查看") 

### 如何开发？
Maixduino支持原始 [Arduino IDE](https://www.arduino.cc/en/Main/Software "Arduino IDE") 的开发，同时也可以选择支持一键调试功能的 [PlatformIO IDE](https://maixduino.sipeed.com/zh/get_started/install.html "PlatformIO IDE") 开发。
开发环境配置

- 正常情况下，win10 ，linux3.0+ ，mac os都可以自动识别并安装串口驱动。如果遇到驱动失败，可以去 FTDI 官网下载对应的 VCP 驱动程序。`https://www.ftdichip.com/Drivers/VCP.htm`
- win驱动下载地址：`http://dl.sipeed.com/MAIX/tools/ftdi_vcp_driver/CDM21228_Setup.zip`
- 如果到驱动安装不正确，请彻底卸载原驱动，下载官方驱动，切断网络并安装驱动即可解决问题。

### 特性

◼ CPU : RISC-V 双核 64bit、内置 FPU、400Mhz 标准频率(可超频)内置神经网络处理器

◼ 连接器 : 兼容 Arduino 接口 24P LCD 连接器 24P 摄像头连接器 TF卡插槽扬声器接口

◼ 开发环境 : 支持 Arduino IDE

◼ 电源输入 : USB 或 DC (6-12V input ; 板载 DC-DC 提供 5V 1.2A 输出 ) 

◼ 下载电路 : 只需要连接 USB typeC 线即可完成 K210 和 ESP32的下载

◼ 8 Bit(256 级) 可调颜色,5Bit (32 级)亮度调节

◼ 无线功能（可选) : 支持 2.4G 802.11.b/g/n 支持 Bluetooth 4.2

◼ 音频功能 : MEMS 麦克风 and 3W 扬声器输出

![](https://mc.dfrobot.com.cn/forum.php?mod=image&aid=105653&size=300x300&key=18e2ae6fad157fdd&nocache=yes&type=fixnone)


| 功能概述 | |
| -------- | -------- | 
| 主要模块   | Sipeed M1 或者 M1W AIOT 模块  |
| 电源输入   | 1. USB Type-C  2. DC-DC 降压电路（支持 6-12V 输入） |
| Micro SD card（TF card） 插槽 | 支持自弹 TF 卡座  |
| 板载 MEMS 麦克风 | MSM261S4030H0 是一个全方位、底部端口、I 2 S 数字输出的MEMS 麦克风。它具有高性能和可靠性。 |
| DVP 摄像头接口 | 24P 0.5mm FPC 连接器：支持 OV2640、5640、OV7740 等等 |
| LCD 接口 | DAC+PA: 1. TM8211：16 bit 动态范围；低谐波失真； 2. NS4150：3W 输出功率；高达 90% 效率;|
| 音频输出 | 24P 0.5mm FPC 连接器；支持 8bit MCU LCD |
| ESP32 模块 | 1. 支持 2.4G 802.11.b/g/n；2. 802.11 n (2.4 GHz) 速率达到 150 Mbps；3. Bluetooth v4.2 全规格，包含传统蓝牙 (BR/EDR) 和低功耗蓝牙 (BLE) |


&nbsp;


| 软件概述 | | 
| -------- | -------- |
| FreeRtos & Standard SDK  | 支持 FreeRtos and Standrad development kit. |
| MicroPython Support | 支持 MicroPython on M1 |
| 机器视觉 | 基于卷积神经网络的机器视觉 |
| 机器听觉 | 高性能麦克风阵列处理器 |

![](https://mc.dfrobot.com.cn/forum.php?mod=image&aid=105654&size=300x300&key=5b33fcc226fc7cab&nocache=yes&type=fixnone)

### 相关文章

- [嵌入式AI从入门到放肆【K210篇】-- 硬件与环境](https://mc.dfrobot.com.cn/thread-299778-1-1.html)

- [【MaixPy 教程】用mixly玩转K210——人脸追踪](https://mc.dfrobot.com.cn/thread-305097-1-1.html)
- [【MaixPy 教程】用mixly玩转K210——20类对象检测](https://mc.dfrobot.com.cn/thread-305125-1-1.html)
- [【MaixPy教程】用mixly玩转K210——调用AI_OneNET API实现车牌识别](https://mc.dfrobot.com.cn/thread-305038-1-1.html)
- [【MaixPy 教程】用mixly玩转K210——一键本地模型训练](https://mc.dfrobot.com.cn/thread-305291-1-1.html)
- [【MaixPY 教程】用mixly玩转k210——MixNo通过TCP/IP与掌控板进...](https://mc.dfrobot.com.cn/thread-305317-1-1.html)

### 活动流程

- **申请**

第一项：请在留言区认真描述如获得评测资格`您将使用此款产品制作什么样的项目`；

第二项：扫描下方二维码，或点击[报名链接](https://jinshuju.net/f/prj5bk "报名链接")填写个人资料。

![报名二维码](https://mc.dfrobot.com.cn/forum.php?mod=image&aid=105731&size=300x300&key=44397bea332185cf&nocache=yes&type=fixnone)

> 请务必详细填写上述两项内容，这将作为选人及之后测评情况跟踪的重要依据，描述不详细者直接不通过申请。

* **筛选**
> ①评测内容基于测评产品，有一定的相关产品使用经验者优先考虑；
>
> ②测评计划及即将要测评的内容详细且具体；
>
> ③综合考虑申请者的论坛积分，活跃情况。

* **名单公布**
> 测评名单将在活动页公布;

* **测评通知**
> 名单公布后工作人员将通知先前提交的个人信息中的联系方式联系申请成功者，3天不回复算弃权;

* **产品寄送**
> 公布测评名单后第一时间将产品快递给大家，将按照申请者提交个人信息中的地址邮寄，请在填写资料时务必确认信息正确并能正常收件;

* **投稿**
> 获得测评资格的用户，需按照申请时的描述将完成的项目投稿至DF创客社区；

* **报告审查**
> 提交过相应的测评报告后，如报告通过要求审核，测评者即可留下测评产品，此时产品拥有权归测评者所有。

### 活动时间&名额

- **报名截止时间**：2020年6月25日00:00

- **名单公布时间**：2020年6月28日12:00

- **名额**：5人

### 活动要求

测评者收到产品后，进行学习评估，并在板块发帖记录测评过程、分享测评心得，内容可以包括：连载的入门教程或者说明；项目分享等……

最终产出文章必须大于等于`* 2 *`篇！！！

**以下类型文章将不计入最终产出文章总数中**：
> 1. 开箱帖；
> 2. 水贴（如：简单的点灯帖）；
> 3. 内含大量该产品现有的介绍、性能等内容的帖子；
> 4. 内含大量与产品和本次测评无关内容的帖子。

### 示范文章链接跳转：

- [LattePanda试用之一体化电子仪器平台—序章(纯灌水)](https://mc.dfrobot.com.cn/thread-24413-1-1.html)

- [基于LattePanda开发板的一体化电子仪器平台——试用体验](https://mc.dfrobot.com.cn/thread-27555-1-1.htm)

- [基于LattePanda开发板的一体化电子仪器平台——制作过程](https://mc.dfrobot.com.cn/thread-27556-1-1.html)

- [基于LattePanda开发板的一体化电子仪器平台——功能参数](https://mc.dfrobot.com.cn/thread-27557-1-1.html)

- [基于LattePanda开发板的一体化电子仪器平台——终篇？](https://mc.dfrobot.com.cn/thread-27554-1-1.html)


### 注意事项

* 测评者所分享所有内容须为原创并在DFRobot创客社区首发;
* 请收到众测产品的小伙伴们务必按时完成原创体验报告。逾期未发者将视为自动放弃活动参与资格，需返还众测产品，同时取消之后的众测活动获选资格；
* 如因突发情况，预估无法继续完成测评，测评者请将测评产品退还至DFRobot创客社区，让其他网友继续试用;
* 产品寄送期间由活动发起方支付产品寄送的费用；但活动过程中若因申请者自身原因产生多余运输费用，此费用由申请者自行支付；
* 活动过程中，产品所有权仍归DFRobot创客社区所有，测评者只拥有使用权;
* 测评产品属于精密电子产品，请测评人员能够爱惜，避免一些不必要的损害。如果在使用过程中出现恶意损坏的行为，测评人员须照价进行赔偿；如报告通过要求审核，测评者即可留下测评产品，此时产品所有权归测评者所有；

本活动最终解释权归DFRobot创客社区所有。

请认真阅读以上内容！