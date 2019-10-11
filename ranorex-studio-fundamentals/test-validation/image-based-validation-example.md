# [译] 基于图像的验证示例

*原文地址 👉 [Image-based validation example][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : XXX*    

---
基于图像验证的简单教程。在使用此示例之前，请确保您熟悉测试验证的基本概念。

**本章导视**


- [在这一章当中](#在这一章当中)
- [下载示例解决方案](#下载示例解决方案)
- [测试定义](#测试定义)
- [录制准备](#录制准备)
- [录制测试：第一部分](#录制测试：第一部分)
- [基于图像的验证](#基于图像的验证)
- [完成录制](#完成录制)
- [结果](#结果)


>**视频向导**         
视频“基于图像的基本验证”将引导您完成本章中的信息。           
[立即观看](https://www.youtube.com/embed/tphkYyBeYvo)

## 下载示例解决方案
要继续学习本教程，请从以下链接下载示例解决方案文件。

**示例解决方案**
>主题：建立测试
>时间：15分钟              
>[点我下载](https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleImageBasedValidation.zip)

### **安装示例解决方案：**
1. 解压缩到计算机上的任何文件夹。

2. 启动 Ranorex Studio并打开解决方案文件ImagebasedValidation.rxsln


>**贴士**            
样本解决方案适用于Ranorex 8.0或更高版本。您必须同意8.2及更高版本的自动解决方案升级。


## 测试定义
在开始录制之前，让我们定义测试。它包括5个步骤：

1. 启动演示应用程序。

2. 点击该图片为基础的自动化选项卡。

3. 使图像可见。

![A8050-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8050-0000010.gif)


4. 验证是否显示图像。

5. 退出演示应用程序。

## 录制准备
1. 使用解决方案向导创建桌面测试解决方案，并在设置的第2步中选择演示应用程序作为AUT。


![A4020-0000051](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A4020-0000051.png)

1. 演示应用程序被选为AUT，并在您开始录制时自动启动。

2. 解决方案向导完成后，单击 Ranorex Studio工作环境中的Recording1选项卡。

## 录制测试：第一部分

>**贴士**         
>请记住，如果您不使用白名单，则一旦开始录制，即使未在AUT上执行，也会捕获所有用户交互。
>- 单击“Pause”  以暂停录制。单击  继续  以继续录制。
>- 单击“Stop”  以结束录制。           
了解有关Ranorex Studio基础知识> Ranorex Recorder> 👉[录制器控制中心和热键][1]的录制仪控制中心的更多信息。        
阅读Ranorex Studio基础知识中的白名单 >  👉[白名单][2]。

1.在Recording1的录像模块视图中，单击RECORD。Ranorex Studio自动最小化到任务栏。
录制器控制中心显示录制处于活动状态。

![A4030-0000031](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A4030-0000031.png)                
*开始测试录制*

2. 被测试的应用程序成为焦点。单击基于图像的自动化选项卡。

3. 要显示图像，请单击复选框显示图像。

![A8050-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8050-0000010.gif)

## 基于图像的验证
示例验证的目标是验证选中复选框时是否显示猫的图像。由于这需要我们验证图像，因此它是基于  图像的验证。

请按照以下步骤动作：

### **激活基于图像的验证**
1. 在Recorder控件中，激活基于图像的开关录制。

2. 单击“Validate”。录像机暂停录制并切换到基于图像的验证模式。


![A8050-0000011](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8050-0000011.png)

### **选择验证元素**
3. 选择要验证的UI元素：
- 将鼠标悬停在猫的图像上。鼠标移动后会出现紫色框。
- 紫色框表示当前选择哪个元素进行验证。
- 选择与图像匹配后，单击它。

![A8050-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8050-0000070.gif)


### **确认验证元素**
4. 要确认UI元素，请单击“Next”。

![A8050-0000021](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8050-0000021.png)

1. GUI中的UI元素位置

- UI元素树表示应用程序的分层GUI结构。
- 如果需要，您可以单击其他UI元素以选择它进行验证。
2. UI元素状态和属性

- 所选UI元素的所有属性都显示在此区域中。


3. 验证UI元素的屏幕截图
- 使用屏幕截图快速检查您是否选择了正确的UI元素。



### **定义验证属性**
5. 定义将用于验证的图像。对于我们的示例，只需保留所有内容，然后单击“OK”进行确认。

![A8050-0000031](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8050-0000031.png)


1. 在“验证”对话框中选择“ 图像”选项卡，而不是“ 属性”选项卡。

2. 使用“包含”验证模式时，绘制一个矩形以选择图像的一部分。

3. 提供不同的图像验证模式：

- None：  停用图像验证。
- Contains： 确定验证图像是否包含在测试期间找到的实际图像中。
- Compare：确定验证图像和测试期间找到的实际图像是否相同。


### **完成录制**
完成验证动作后，Ranorex会自动继续录制。下一步是结束测试录制。

![A8050-0000041](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8050-0000041.png)

1. 在“Recorder”控制中心中，单击“Stop”以结束录制。

## 结果
录制停止后，您将返回Ranorex Studio。您将看到包含三个录制动作的动作表。动作＃3是验证动作。

![A8050-0000051](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8050-0000051.png)           
*录制基于图像的验证示例的结果*

1. 验证类型运算符

- 此运算符标识要执行的验证类型。
- 有九种不同的验证类型运算符。

![A8050-0000061](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8050-0000061.png)             
*用于基于图像的验证的验证类型运算符*

>**章节预览**              
有关所有验证匹配运算符的详细说明，请参见>  Ranorex Studio基础知识>动作>  👉[动作属性][3]。

2. 将匹配测试期间找到的实际图像的验证屏幕截图。
3. 动作链接到控件库项，即执行验证的UI元素。

### **解释验证**
作为陈述书写，验证内容如下：

如果在控件库项引用的UI元素中Screenshot1包含（ContainsImage）TheCat，那么验证将返回值' True'。


---  

[👈基于属性的验证示例][4]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[验证工具提示👉][5]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/test-validation/image-based-validation-example/
[1]: .\ranorex-recorder\recorder-hotkeys.html
[2]: .\whitelisting\whitelisting.html
[3]: .\actions\action-properties.html
[4]: .\attribute-based-validation-example.html
[5]: .\validation-tool-tips.html