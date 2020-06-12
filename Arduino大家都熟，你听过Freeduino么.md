---
title: Arduino大家都熟，你听过Freeduino么
top: true
categories:
  - 创客项目
cover: https://mc.dfrobot.com.cn/data/attachment/forum/202004/28/151818ndl9l2amd0ld9l4v.png
abbrlink: 2726196329
date: 2019-12-20 14:48:36
tags:
toc_number:
toc:
top_img:
description:
keywords:
copyright: true
---
![“骨架型”Arduino Uno](https://mc.dfrobot.com.cn/data/attachment/forum/202004/28/151818ndl9l2amd0ld9l4v.png)

是的，我确实做到了。很难，花了我几天时间，但我做到了。最后，这是一次很棒的体验，最令人惊讶的是Freeduino确实有效。我想与您分享我的经验。

什么是Freeduino？它就是没有任何电路板的Arduino UNO板·。它使用一种称为自由形式的技术通过导线或铜丝而不是电路板来互连组件。它看起来简约又漂亮！

为什么我要做这个？我经常很难解释什么是自由形式的电子及其外观。而Freeduino正好是自由形式电子艺术的一个很好的例子，可以轻松地与著名的设备Arduino UNO相提并论，因此我做了它。

你可以查看上一篇LED珠宝，了解黄铜焊接的基础知识，所需的工具和材料。

## 了解Arduino UNO电路
![](https://mc.dfrobot.com.cn/data/attachment/forum/202004/28/151859rb47be7mw7bezw2o.png)
在实际开始焊接之前，我们需要了解Arduino UNO的各部分功能。大体可以将其分为4个块：

#### ATmega328 MCU

- ATmega328P PDIP
- 16MHz振荡器
- 防抖电容器

#### 电源电路

- 7-12V至5V电压调节器
- 5V至3.3V电压调节器
- USB /输入插孔自动选择电路
- 反向电流保护

#### USB转UART电路

- USB接头
- 带有振荡器和去抖电容器的串行转换器芯片（ATMEGA8U2-MU）

#### 信号灯

- 电源指示灯
- 默认LED（D13）
- TX / RX LED

## ATmega328 MCU
首先，我们·从MCU以及数字和模拟IO引脚接头开始。Arduino UNO具有巧妙的排针布局，与ATMEGA328 28-DIP封装的布局非常匹配。因此，无需交叉导线。
![Arduino UNO引脚图](https://mc.dfrobot.com.cn/data/attachment/forum/202004/28/151942w6tpofy0ykywk76h.png)
![](https://mc.dfrobot.com.cn/data/attachment/forum/202004/28/152113xniuzrccnhvxhnif.png)

ATmega328起作用的唯一外部组件是需要两个22pF电容器的外部16MHz振荡器。ATmega328P的硬件最少。现在可以通过AVR ISCP接口与USBasp编程器进行第一次测试。

![](https://mc.dfrobot.com.cn/data/attachment/forum/202004/28/152219tqtdwthtktcaw42t.png)

## 电源电路
我给自己做了一个特殊的夹具，用于将针座固定在适当的位置，从而留出足够的焊接空间。
![定制夹具将针座固定在适当的位置](https://mc.dfrobot.com.cn/data/attachment/forum/202004/28/152308lhqaphu8p6rqjsem.png)

ATmega328由5V供电。Arduino UNO有两个电源输入源——插孔（7-12V）或USB连接器（5V）。同时它还为外部组件提供3.3V电源。这意味着需要2个稳压器。首先将7-12V转换为5V，然后将5V转换为3.3V。根据数据手册中的建议，我使用了两个AMS1117 5V和3.3V稳压器以及一些电容器。
![](https://mc.dfrobot.com.cn/data/attachment/forum/202004/28/152429zkk9rqozz90z0kvk.png)
为了简化操作，我将电源电路焊接到了板子的外部，然后将其放在数据线上。这实际上创建了两层自由形式的电路。我省略了自动选择和反向电流保护部分，因为这会使所有过程变得非常复杂。除非您对板子不满意，否则可以不需要它们。


## USB转UART电路
![CH340C USB转UART转换器](https://mc.dfrobot.com.cn/data/attachment/forum/202004/28/152450nokhecd4ieenwj43.png)

如果要在不依赖程序员的情况下通过Arduino IDE上传程序，这一点很重要。好吧，没有它就不会那么酷。原始的Arduino UNO R3使用ATMEGA8U2-MU，虽然很棒，但太小了，不适合自由形式的电路。我决定选择CH340C芯片。它具有合适的SOP-16封装，仅需四个外部组件——去抖电容器，复位电容器和两个Tx / Rx线路电阻器。无需外部电容器的事实大大简化了整个电路。
![](https://mc.dfrobot.com.cn/data/attachment/forum/202004/28/152506vq327oxxolq2c4r3.png)

## LED指示灯
我不喜欢那些大型THT LED，所以我决定使用小型SMD 1206 LED来发出功率，L，Tx和Rx通信信号。我很后悔。我先将一个SMD电阻焊接到他们，然后尝试将其焊接到电线。这很棘手。我必须使用低温的烙铁，并尽快解决问题，否则SMD组件的另一侧会被拆焊。
![](https://mc.dfrobot.com.cn/data/attachment/forum/202004/28/152526b0auzpuaptqfz29t.png)

## Freeduino能点亮吗？
首先，我连接了外部电源来检查电源调节器。所有电压电平都很好，因此我继续进行连接，并通过USBasp编程器将自举程序上传到芯片中。惊喜的是，该芯片在第一次尝试时就进行了通信。那是一个好兆头。外部晶振正常工作，所有引脚均正确连接。最后一步是连接USB电缆，然后尝试上传blink的程序。我们来看看：

<iframe height=498 width=100% src="//player.bilibili.com/player.html?aid=79924326&cid=136787174&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

现在，我将其装入透明树脂中，以使其不那么脆弱。
![与原始Arduino UNO的合影](https://mc.dfrobot.com.cn/data/attachment/forum/202004/28/152546znrefqyq0gyq5f6s.png)
![仰视图来一张](https://mc.dfrobot.com.cn/data/attachment/forum/202004/28/152611reaeiqcpdsadff1x.png)
![俯视图再来一张](https://mc.dfrobot.com.cn/data/attachment/forum/202004/28/152629f95gjg2b4souioax.png)

我是Jiri Praus。
欢迎访问我的网站www.jiripraus.cz
