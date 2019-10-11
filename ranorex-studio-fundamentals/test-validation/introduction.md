# [译] 测试验证
    

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月10日-green.svg?longCache=true&style=flat-square)


---

在软件测试中，验证是验证被测应用程序产生的动作和/或响应是否与预期结果匹配的过程。本章介绍Ranorex Studio中提供的测试验证方法。

为简单起见，本章演示了使用常量值来确定应用程序是否返回预期结果的验证。实际上，您通常希望使用变量进行验证而不是常量值。

>**贴士**         
要了解如何在验证操作中使用变量，请参阅以下部分：                
Ranorex Studio高级>变量和参数>  👉[验证变量][1]。


**本章导视**

- [了解验证](#了解验证)
- [间接验证](#间接验证)
- [验证过程](#验证过程)
- [激活验证](#激活验证)
- [选择验证元素](#选择验证元素)
- [确认验证元素](#确认验证元素)
- [定义验证属性](#定义验证属性)
- [验证示例](#验证示例)






## 了解验证
让我们从一个简单的测试验证示例开始。想象一下你用来添加两个数字的标准袖珍计算器：

![A8010-0000011](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8010-0000011.png)         
*示例计算*

如果计算器返回预期结果，则测试验证成功，57.79。
然而，袖珍计算器的制造商需要保证不仅这个结果是正确的，而且还要保证所有其他结果，从最简单的添加到任何其他复杂的内置数学公式。

这是测试验证发挥作用的地方。自动化测试可以根据需要使用不同的输入数据和结果覆盖尽可能多的不同计算，以证明计算器正常工作。

## 间接验证
重要的是要了解GUI测试自动化仅提供间接测试验证。这意味着我们验证用户输入的序列是否为：

![A8010-0000021](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8010-0000021.png)

导致结果：

![A8010-0000031](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8010-0000031.png)

间接验证验证显示的结果与基于用户输入的预期结果类似。它无法确保计算器是否正常工作。
- 用户输入和屏幕上结果的显示之间可能存在许多操作和处理步骤。
- 我们只能将显示的结果与用户输入操作的初始序列进行匹配，并确定结果或动作是否符合预期。


换句话说，如果测试验证失败，则没有证据表明出现了什么问题。它可能是软件正确处理所有内容，但结果显示有点错误。测试数据可能包含错误数据。您始终需要注意，我们无法验证计算机系统中的内部处理步骤，而只能验证“外部”可见结果。在设计测试用例时请记住这一点。

## 验证过程

测试验证是一个包含四个连续步骤的过程，如下所示。您可以在录制期间创建测试验证操作，也可以稍后手动添加。

![A8010-0000041](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8010-0000041.png)         
*这是图像的标题*

## 激活验证
在Ranorex中，验证被视为一种特殊类型的操作。因此，“激活”测试验证只是意味着将验证操作添加到当前录制模块。以下说明描述了在录制会话期间添加测试验证。如前所述，还可以在录制后手动添加验证操作。

>**贴士**                
如果您不熟悉测试操作，我们建议您阅读
Ranorex Studio基础知识👉[动作][2]

![A8010-0000051](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8010-0000051.png)        
*激活验证*

1. 要配置基于文本的验证：

- 单击“Validate”以激活基于文本的验证模式。


2. 要配置基于图像的验证：

- 激活开关基于图像的录制。
- 单击“Validate”以激活基于图像的验证模式。

>**贴士**          
录制会话会自动暂停，以允许您插入测试验证操作。这由录制器控制中心的紫色条表示。

## 选择验证元素

验证过程的第二步是选择要验证的UI元素。选择过程与验证类型无关（即文本/属性/基于图像的验证）。

将鼠标移到要验证的UI元素上。寻找在UI元素周围出现的紫色框架，表明Ranorex Studio已经识别出它。单击以选中UI元素。

![A8010-0000061](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8010-0000061.png)

1. 选择基于文本的验证元素。

2. 选择基于图像的验证元素。


>**贴士**
>- 识别正确的UI元素可能具有挑战性，尤其是当它与其他UI元素紧密嵌套时。
>- 如果您错误地选择了错误的UI元素，则可以在下一步中轻松更改它。


## 确认验证元素

验证过程的第三步是确认选择了正确的UI元素进行验证。如果是这样，单击下一步。否则，请更正选择。

### **确认对话框组件**

![A8010-0000071](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8010-0000071.png)            
*验证确认对话框的组件*


1. GUI中的UI元素位置
- Ranorex识别被测应用程序中的每个UI元素。
- 所有UI元素都以分层结构进行管理。
- UI元素的名称源自其基础类型和内容。


2. UI元素状态和属性

- 每个UI元素由一组属性和状态定义。
- 状态的示例是Enabled，其当前值为True。
- 属性的示例是UI元素的名称。在上面的示例中，text属性具有当前值lblWelcomeMessage。

3. UI元素的屏幕截图

- 显示所选UI元素的屏幕截图以进行确认。


>**贴士**            
UI元素，它们在Ranorex中的表示以及它们的状态和属性都包括在内               
Ranorex Studio高级>  👉[UI元素][3]

### **确认动作**

![A8010-0000081](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8010-0000081.png)             
*单击下一步以确认验证元素*

1. 确认基于文本的验证元素。
2. 确认基于图像的验证元素。


### **定义验证属性**
每个UI元素由状态和属性定义。在最后一步中，指定要用于验证的特定属性或状态，如下所示。

![A8010-0000091](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8010-0000091.png)              
*验证UI元素的属性/子图像选择*

1. 基于文本/属性的验证的属性/状态选择

- 可以选择任何可用的属性/状态。
- text属性是基于文本的验证的默认属性。
- 选择属性，然后单击“OK”进行确认。


2. （子）的图像选择为图像 - 基于验证

- 可以通过在图像内绘制粉红色矩形来选择图像的子区域。
- 如果未选择子区域，则完整图像将用于测试验证。


3. 图像验证模式

- 无=没有基于图像的验证; 验证被丢弃。
- Contains =检查匹配的图像是否包含在参考验证图像中。
- 比较=检查匹配的图像与完整的参考验证图像。



##  验证示例
要了解有关这三种验证类型的更多信息，请参阅下面链接的示例：

>**贴士**            
验证示例：              
👉基于文本的验证示例[4]
👉基于属性的验证示例[5]
👉基于图像的验证示例[6]

>**章节预览**          
要了解有关UI元素的更多信息，请参阅            
Ranorex Studio高级>  👉[UI元素][3]。                
要了解有关基于图像的自动化的更多信息，请参阅                    
Ranorex Studio高级>  👉[基于图像的自动化][4]。

---

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[基于文本的验证示例👉][4]




[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/test-validation/introduction/

[1]:.\ranorex-studio-advanced\variables-parameter\validation-variables.html
[2]:.\actions\introduction.html
[3]:.\ranorex-studio-advanced\ui-elements\introduction.html
[4]:.\text-based-validation-example.html
[5]:.\attribute-based-validation-example.html
[6]:.\image-based-validation-example.html
[7]:.\ranorex-studio-advanced\image-based-automation\introduction.html