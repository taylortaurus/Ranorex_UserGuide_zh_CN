# [译] 追踪按钮


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月19日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月29日-green.svg?longCache=true&style=flat-square)


---

在此页面上，您将找到如何从Ranorex Studio中的记录模块或控件库文件中的“追踪”按钮追踪和标识单个UI元素。

**本章导视**

- [测试示例定义](#测试示例定义)
- [追踪按钮](#追踪按钮)
- [结果](#结果)
- [追踪按钮的追踪机制](#追踪按钮的追踪机制)

**视频向导**
>视频的“追踪按钮”将带您了解本章中的信息。             
[立即观看](https://www.youtube.com/embed/3nMU9rl91F8)

## 测试示例定义
为了解释使用“追踪”按钮进行追踪，我们将使用Ranorex Studio演示应用程序的“测试”数据库。

![B3020-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B30/B3020-0000010.png)

1. 演示应用程序中的“测试数据库”选项卡。

2. 测试数据库的工作环境。

## 追踪按钮
追踪按钮在不同位置可用：

- 在资源库工具栏中打开的录制模块中
- 在打开的控件库文件中
- 在Ranorex Spy中


**注意**
>前两个“追踪”按钮的功能相同。您可能会更频繁地使用第一个，这就是我们在此页面上重点介绍它的原因。               
Spy中的“追踪”按钮的工作原理略有不同，这就是我们在“ Ranorex Spy”一章中单独解释的原因。

1. 启动演示应用程序，然后单击“测试数据库”选项卡。

2. 启动 Ranorex Studio并创建一个新的空白解决方案。

3. 打开默认的录制模块，然后单击控件库工具栏中的“ 追踪...”按钮。

![B3030-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B30/B3030-0000010.png)


4. Ranorex Studio已最小化。在演示应用程序中，将鼠标悬停在“ 女性”单选按钮上，然后在红色框周围按一下时单击它，如下所示。 

![B3030-0000020](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B30/B3030-0000020.png)


**注意**
>您只能以这种方式追踪一个元素。追踪此元素后，您将返回Ranorex Studio。要追踪另一个元素，您需要重复该过程。

## 结果
追踪并确定了UI元素后，追踪过程结束，您将返回Ranorex Studio。在这里，您可以看到UI元素的已创建控件库项目。

![B3030-0000030](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B30/B3030-0000030.png)


1. 控件库包含控件库项目RdbFemale。该控件库项目代表“女性”单选按钮，是追踪过程的结果。

2. 控件库项目的RanoreXPath。此路径标识UI元素在AUT的UI中的位置。

## 追踪按钮的追踪机制
- 当您单击“追踪”按钮时，追踪过程将开始，并准备好追踪和标识一个UI元素。
- 追踪一个UI元素后，追踪过程自动结束。
- 在追踪过程中按F12可以暂停追踪。这使您可以单击元素而不追踪它们。这样，您可以追踪隐藏在需要首先打开的下拉列表或菜单中的UI元素。

![B3030-0000040](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B30/B3030-0000040.png)

1. 在追踪过程中按F12可以从演示应用程序的下拉列表中追踪菜单项“ 项目管理”。

---

[👈录制追踪][1]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[即使追踪👉][2]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/tracking-ui-elements/track-button/
[1]:.\track-by-recording.html
[2]:.\instant-tracking.html