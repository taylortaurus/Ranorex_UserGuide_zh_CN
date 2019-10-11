# [译] 基于文本的验证示例
 

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月10日-green.svg?longCache=true&style=flat-square)


---
本章使用一个简单的例子来解释基于文本的验证的概念。在使用此示例之前，请确保您熟悉[测试验证的基本概念][1]。

**本章导视**
- [下载示例解决方案](#下载示例解决方案)
- [测试定义](#测试定义)
- [基于文本的验证](#基于文本的验证)
- [结果](#结果)


>**视频向导**         
>截屏视频“基于文本的验证”将引导您完成本章中的信息。       
[立即观看](https://www.youtube.com/embed/eerGaxTHQl8)

## 下载示例解决方案
要按照本章中的步骤动作，请从以下链接下载示例解决方案文件。

**示例解决方案**
>主题：录制一个测试
>时间：10min以内                
>下载：[点我下载](https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleIntroduction.zip)

### **安装样品溶液：**

1. 解压缩到计算机上的任何文件夹。

2. 启动Ranorex Studio并打开解决方案文件Introduction.rxsln

>**贴士**      
样本解决方案适用于Ranorex 8.0或更高版本。您必须同意8.2及更高版本的自动解决方案升级。


## 测试定义
在我们开始录制测试之前，让我们来定义它。测试包括5个步骤：

1. 打开 Ranorex演示应用程序。

2. 在“Enter your name”字段中，输入Harry并单击“Submit”。

![A1040-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A1040-0000030.gif)

在演示应用程序中更改欢迎消息
3. 验证欢迎消息是否相应更改。

4.  重置  欢迎消息。

5.  结束  演示应用程序并停止  录制。

## 基于文本的验证

此示例中的测试验证的目的是验证我们的测试定义的步骤＃2中的交互是否导致期望的结果，即欢迎消息是否相应地改变。由于这需要我们验证文本字段中包含的文本，因此我们正在执行基于文本的验证。

我们来看看这些步骤：

### **激活验证**
1. 单击“Validate”。录制暂停，录制器切换到验证模式。

![A1050-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A1050-0000030.png)


### **选择验证元素**

2. 选择要验证的UI元素：

- 将鼠标移到已更改的欢迎消息上 鼠标移动后会出现紫色框。
- 紫色框表示当前选择哪个元素进行验证。
- 选择与欢迎消息匹配后，单击它。

![A8030-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8030-0000010.gif)

### **确认验证元素**
3. 要确认UI元素，请单击“Next”。

![A8010-0000071](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8010-0000071.png)

1. GUI中的UI元素位置

- 在这里，您可以通过选择任何其他UI元素进行验证来更正先前的选择。
- UI元素树表示应用程序的分层GUI结构。


2. UI元素状态和属性
- 这里，显示所选UI元素的所有属性。


3. 验证UI元素的屏幕截图

- 使用屏幕截图快速检查您是否选择了正确的UI元素。


### **定义验证属性**
4. 通常预先选择Text属性。如果不是，请选择它。单击“OK”以确认。

![A8030-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8030-0000090.png)


1. 选择文本作为验证属性。

2. 其他可用于验证的属性。

>**贴士**         
描述和定义UI元素的所有属性和状态都可以在验证中使用。您还可以一次验证多个属性和状态，以使验证更具体。


## 结果
完成的录制包含五个动作。动作＃4是验证动作。

![A8030-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8030-0000100.png)           
*录制基于文本的验证示例的结果*

1. 验证动作

2. 验证类型动作符

- 该运算符定义将执行哪种类型的验证。
- 有9种不同的验证类型运算符。

![A8030-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8030-0000110.png)           
*验证类型运算符*

>**章节预览**              
有关所有验证类型运算符的详细说明，请参阅Ranorex Studio基础知识>动作>  👉[动作属性][2]。

3. 验证属性

- 第4列显示验证属性。
- 在我们的示例中，这是Text属性。
- 您可以从下拉菜单中选择其他属性。
4. 匹配值

- 匹配值可以是常量（即文本，数字等）或变量。
5. 链接的控件库项目

- 第6列显示了动作链接到的控件库项，即执行验证的UI元素。

### **解释验证**
详细说明，验证内容如下：

如果Text引用的UI元素的属性LblWelcomeMessage等于（AttributeEqual）欢迎，Harry！“然后验证返回值True。

---
[👈简介][1]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[基于属性的验证示例👉][3]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/test-validation/text-based-validation-example/
[1]:.\introduction.html
[2]:.\actions\action-properties.html
[3]:.\attribute-based-validation-example.html