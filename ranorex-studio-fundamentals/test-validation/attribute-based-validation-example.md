# [译] 基于属性的验证示例

   

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月10日-green.svg?longCache=true&style=flat-square)

---
在本章中，我们将基于一个简单的例子演示基于属性的验证的概念。在使用此示例之前，请确保您熟悉[测试验证的基本概念][1]。

当然，👉[基于文本的验证][2]也是基于属性的验证的一个例子，但我们专门为它设置了一章，因为它可能是最常见的验证类型。
 

**本章导视**


- [下载示例解决方案](#下载示例解决方案)
- [测试定义](#测试定义)
- [录制准备](#录制准备)
- [录制测试：第一部分](#录制测试：第一部分)
- [基于属性的验证](#基于属性的验证)
- [完成录制](#完成录制)
- [结果](#结果)

>**视频向导**             
视频“基于属性的验证”将引导您完成本章中的内容。           
[立即观看](https://www.youtube.com/embed/SEUG3JqAvsM)


## 下载示例解决方案
要继续学习本教程，请从以下链接下载示例解决方案文件。


**下载示例解决方案**
>主题：建立测试
>时间：15分钟                
>[点我下载](https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleAttributeBasedValidation.zip)











### **安装示例解决方案**：

1. 解压缩到计算机上的任何文件夹。

2. 启动 Ranorex Studio并打开解决方案文件AttributeBasedValidation.rxsln


**贴士**             
>样本解决方案适用于Ranorex 8.0或更高版本。您必须同意8.2及更高版本的自动解决方案升级。


## 测试定义
在我们开始录制测试之前，让我们来定义它。测试包括5个步骤：

1. 打开 Ranorex Studio演示应用程序。

2. 单击选项卡UI元素测试区域。

3. 单击单选按钮组框中的单选按钮Green light。

4. 确认单选按钮旁边出现绿色方块。

5. 结束演示应用程序并停止录制。


![A8040-0000011](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8040-0000011.png)            
*基于属性的示例测试定义*

## 录制准备
1. 使用解决方案向导创建桌面测试解决方案，并在设置的第2步中选择演示应用程序作为AUT。

![A4020-0000051](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A4020-0000051.png)

1.演示应用程序被选为AUT，并在您开始录制时自动启动。

2.解决方案向导完成后，单击 Ranorex Studio工作环境中的Recording1选项卡。

## 录制测试：第一部分

**贴士**          
>请记住，如果您不使用白名单，则一旦开始录制，即使未在AUT上执行，也会捕获所有用户交互。
>- 单击“Pause”以暂停录制。单击继续以继续录制。
>- 单击“Stop”以结束录制。                
了解有关更多录制器控制中心和热键：Ranorex Studio基础知识> Ranorex Recorder> 👉[录制器控制中心和热键][4]
阅读Ranorex Studio基础知识中的白名单 > 👉[白名单][5]。

1. 在Recording1的录像模块视图中，单击RECORD。Ranorex Studio自动最小化到任务栏。
录制器控制中心显示录制处于活动状态。

![A4030-0000031](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A4030-0000031.png)        
*开始测试录制*

2. 被测试的应用程序成为焦点。

3. 在单选按钮组框中，单击单选按钮`Green light`。

![A8040-0000021](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8040-0000021.png)


## 基于属性的验证
此示例中的测试验证的目的是在单击单选按钮后验证彩色方块是否以正确的颜色显示。

由于这需要我们验证UI元素的颜色属性，因此我们正在执行基于属性的验证。

我们来看看这些步骤：

### **激活验证**
1. 单击“Validate”。录制暂停，录制器切换到验证模式。

![A8040-0000031](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8040-0000031.png)


###  **选择验证元素**
2.选择要验证的UI元素：

- 将鼠标悬停在绿色方块上。鼠标移动后会出现紫色框。
- 紫色框表示当前选择哪个元素进行验证。
- 选择与绿色方块匹配后，单击它。

![A8040-0000041](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8040-0000041.png)

### **确认验证元素**
3. 要确认UI元素，请单击“Next”。

![A8040-0000051](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8040-0000051.png)

1. 选定的验证元素：
- UI元素具有角色Container和ControlName pnlColourPanel
2. 所选UI元素的屏幕截图，显示绿色方块。


### **定义验证属性**
4. 选择Exists（通常是预选）和BackColor属性，然后单击OK确认。

![A8040-0000061](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8040-0000061.png)

1. General属性里的 Exists通常被预选。
2. 将Dynamic属性里的带着Green值得BackColor选上


## 完成录制
完成验证动作后，Ranorex会自动继续录制。下一步是结束测试录制。

![A8040-0000071](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8040-0000071.png)           
*在“Recorder”控制中心中，单击“Stop”以结束录制。*


## 结果
录制停止后，您将返回Ranorex Studio。动作表包含三个录制的动作。动作＃3是验证。 

![A8040-0000081](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8040-0000081.png)                                           
*录制基于属性的验证示例的结果* 

1. 验证动作

2. 验证类型动作符

- 此运算符标识要执行的验证类型。
- 有九种不同的验证类型运算符。

![A8030-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8030-0000110.png)          
*验证类型运算符*

>**章节预览**     
有关所有验证匹配运算符的详细说明，请参阅Ranorex Studio基础知识>动作>  👉[动作属性][6]。
 

3. 验证属性：

- 此列显示验证属性。
- 在我们的示例中，这是BackColor属性。
- 您可以从下拉菜单中选择其他属性。
4. 匹配值：

- 匹配值可以是常量（即文本，数字等）或变量。
5. 控件库项目：

- 此列显示链接到动作的控件库项，即执行验证的UI元素。


### **解释验证**
如果作为陈述书写，则验证内容如下：

如果属性BackColor的UI元素的PnlColourPanel是EQUAL的值Green，THEN验证返回值“ True”。

---

[👈基于文本的验证示例][2]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[基于图像的验证示例👉][3]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/test-validation/attribute-based-validation-example/
[1]:.\introduction.html
[2]:.\text-based-validation-example.html
[3]:.\image-based-validation-example.html
[4]:.\ranorex-recorder\recorder-hotkeys.html
[5]:.\whitelisting\whitelisting
[6]:.\actions\action-properties.html