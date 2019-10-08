# [译] 录制追踪


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月19日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月29日-green.svg?longCache=true&style=flat-square)

---


在Ranorex Studio中录制测试步骤时，会自动跟踪UI元素，因此在对它们执行操作时会被标识。这是通过录制进行跟踪。如果您已阅读Ranorex Studio基础知识中的各章，则您应该已经熟悉此方法。我们将通过一个简单的示例在此页面上再次对其进行快速浏览。


**本章导视**

- [测试示例定义](#测试示例定义)
- [录制跟踪](#录制跟踪)
- [结果](#结果)
- [通过录制进行跟踪的跟踪机制](#通过录制进行跟踪的跟踪机制)



**视频向导**
>视频“按录制跟踪”将带您了解本章中的信息。                  
[立即观看](https://www.youtube.com/embed/eUBubjWEzZY)

## 测试示例定义
为了解释通过录制进行跟踪，我们将在Ranorex Studio演示应用程序的Test数据库中录制对UI元素的单击。

![B3020-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B30/B3020-0000010.png)


1. 演示应用程序中的“测试数据库”选项卡。

2. 测试数据库的工作环境。

## 录制跟踪
现在，让我们看看通过录制进行跟踪的实际方式。

1. 启动演示应用程序，然后单击 “测试数据库”选项卡。

2. 启动 Ranorex Studio并创建一个新的空白解决方案。

3. 打开默认的录制模块，然后单击RECORD。

4. Ranorex Studio消失，并出现Recorder控制中心，表明正在录制。

![B3020-0000020](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B30/B3020-0000020.png)

5. 在“测试数据库”选项卡中，单击 “ 女性”单选按钮。

![B3020-0000030](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B30/B3020-0000030.png)


6. 单击“录制器”控制中心中的“停止”。

## 结果
停止录制后，Ranorex Studio将显示带有操作表和当前控件库的录制模块视图。

![B3020-0000040](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B30/B3020-0000040.png)

1. 链接到代表女性单选按钮的控件库项目RdbFemale的鼠标单击操作。

![B3020-0000050](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B30/B3020-0000050.png)



2. 控件库包含控件库项目RdbFemale。该控件库项目代表“女性”单选按钮，是跟踪过程的结果。

3. 控件库项目的RanoreXPath。此路径标识UI元素在AUT的UI中的位置。

## 通过录制进行跟踪的跟踪机制

- 在录制时，Ranorex Studio监视用户与UI的交互并自动跟踪UI元素。
- 发生用户交互时，Ranorex Studio会识别目标UI元素并将其存储为控件库项，该控件库项是UI元素的表示。
- 通常，一个控件库项代表一个UI元素。
- Ranorex Studio识别何时多次使用UI元素，然后重用相应的控件库项目。

---

[👈简介][1]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[跟踪按钮👉][2]


[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/tracking-ui-elements/track-by-recording/
[1]:.\introduction.html
[2]:.\track-button.html