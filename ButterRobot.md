# 造一个黄油机器人(Butter Robot)

上次制作了[Rick的传送枪](https://mp.weixin.qq.com/s/I5LkhMr3CZ_kK2MXG-DFvQ)，这次我们来做个大一点的活，就是黄油机器人(Butter Robot)了。

我觉得一个Rick and Morty的粉丝兼一名Maker 一定会制作这一个剧中最受欢迎的机器人。

以下是黄油机器人Butter Robot的造型与设计图纸。

![](https://imgkr.cn-bj.ufileos.com/6bdceb38-17b1-44e4-97a7-99aee4122b8d.gif)




![](https://imgkr.cn-bj.ufileos.com/bb2575f6-8843-4289-a24c-bfa798b9108d.png)



![Rick and Morty中机器人的图纸](https://imgkr.cn-bj.ufileos.com/15e97e37-71d1-4e25-a54c-c1228e70759a.png)

## 第1步，3D模型设计

![](https://imgkr.cn-bj.ufileos.com/67fe8362-fa25-4aa5-9944-fd5f7b51660f.png)

在3DSMAX设计出黄油机器人(Butter Robot)的外形，如下图所示。 它的结构分为以下几个部分：


![](https://imgkr.cn-bj.ufileos.com/4c37d998-0076-45ac-9c60-b6cc3c3919fe.png)

（1）头部，主要用于隐藏大部分的电子电路；

（2）小车部分，有两个电机，4个1.5V与一个9v的电池都在里面；

（3）舵机支架，中间有舵机，连接头部与小车。


以下就是3DSMAX出来的效果与实际的对比:

![](https://imgkr.cn-bj.ufileos.com/52365035-e1e2-48d0-bae5-2091246249ba.png)

## 第2步,准备电子材料 

与以往的风格一样，这个装置现在会用到Arduino mini（尺寸比较小）外加一个电机控制小板子DRV8833，会基本电路就可以安装了。

### 材料如下：


![](https://imgkr.cn-bj.ufileos.com/16cd8c01-963e-4884-af33-1e79773e5d0f.png)

- 1个9V的电池给ARDUINO供电
- 1个ARDUINO MINI 板，
- 几片孔洞板，用于制作LED灯与外接接收的外接电路
- 电焊铁，电线（杜邦线）
- 小型开关2个,一个用来打开ARDUINO板，一个控制电池供电
- 1个红外接收器与1个红外控制器
- 1个LED灯，用来显示红外的接收情况
- 1个舵机，控制头部的活动
- 2个小黄电机，控制机器人的活动
- 电线若干。其它就是用3D打印机打印。材料就是相对多一点，

经过训练的朋友都能做这个小型装置。

## 第3步,分开模块与打印 

在3DSMAX将不同颜色不同部分的组件分别排版。

如下图所示：


![](https://imgkr.cn-bj.ufileos.com/43c913c6-6eb0-4dcb-8445-1d84b0a87074.png)

采用了不同颜色的线材，包括银色，灰色（由于银色比较难找，所以采用喷漆）

![](https://imgkr.cn-bj.ufileos.com/51895ef1-30e4-44e4-bce0-18e7dde9abc5.png)

3D打印机采用 XYZprinting Mini Maker，如下图所示。

![](https://imgkr.cn-bj.ufileos.com/eb7765b7-f362-4893-99ad-09d798bf12f5.png)

## 第4步,电子电路的设计与制作 

以下是电路图的设计，分为三部分，

![](https://imgkr.cn-bj.ufileos.com/44d82212-74e4-460e-b5da-fe4dbd95435b.png)

基本采用ARDUINO实例教程的基本组合：

- 红外接收电路（增加一个LED显示状态）
- 舵机电路（ARDUINO直控）
- 小黄电机电路（用到DRV8833板子）

如下图所示，通过焊接电线与孔洞板，实现了整个电路的连接，完成图如下:


![](https://imgkr.cn-bj.ufileos.com/42ae9b5a-198e-457d-a03a-46fbf363cee0.png)

## 第5步,模块的组装
对构件进行粘合，采用强力胶对部份构件进行连接，如下图所示。

其它部位不需要采用胶水连接，直接采用M3X10的螺线连接就可以了。

其中，头部的两根电线是装饰没有功能。

## 第6步,写入ARDUINO的编程代码
对ARDUINO板写入代码，这个代码就是就是ARDUINO板实现读取红外信号，

实现电机转动与舵机动作的代码。

[点击下载](https://aipicu.lanzous.com/ivBo6dglq0b)

## 第7步,最后的测试 

以上是Butter Robot的最后完成图：


![](https://imgkr.cn-bj.ufileos.com/110df1cb-5bba-40cd-9345-7d45e034c9c2.png)

打开小开关可以启动机器人了，通过控制器可以控制它，以下是动画的全部过程：



![](https://imgkr.cn-bj.ufileos.com/2d95b032-5c3d-40fa-8ffe-e3afb507f904.gif)


项目作者：dinochen1983

项目来源：DF创客社区论坛




