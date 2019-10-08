# [译] 数据驱动测试


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月14日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月27日-green.svg?longCache=true&style=flat-square)

 
---

在数据驱动的测试中，测试容器（测试用例/智能文件夹）从数据源（例如Excel电子表格或数据库文件）中检索输入值。然后针对数据源中的每一行数据自动重复测试容器。

数据驱动测试的关键组件是变量，数据源和数据绑定。在接下来的章节中，您将学习如何将它们结合起来以构建数据驱动的测试。示例解决方案和随附的说明将指导您完成该过程。

参数是数据驱动测试的另一个组成部分。它们提高了模块的可重用性，并使可变值从一个录制模块传递到另一个录制模块成为可能。

数据驱动的测试还允许您使用条件来进一步控制测试的执行，这就是为什么在数据驱动的测试章节的末尾解释了此主题的原因。

**本章导视**

- [下载样本解决方案](#下载样本解决方案)
- [数据驱动测试的过程](#数据驱动测试的过程)
- [知识点推荐](#知识点推荐)  


&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[定义变量👉][7]


**观看我们的点播网络研讨会**

精通数据驱动测试：如果您喜欢视频说明，还可以观我们的看点播网络研讨会。了解如何设置变量并将其链接到数据源。您还将学习数据绑定如何将变量连接到数据项，如何用条件控制执行以及如何通过模块边界和跨测试用例传递值。        
[现在观看](https://www.ranorex.com/automated-testing-webinars/mastering-data-driven-testing/)

**视频向导**
>视频“什么是数据驱动测试？”将带您逐步了解本章中的信息。         
[立即观看](https://www.youtube.com/embed/Yl3NjiJicDY)


## 下载样本解决方案

通除了有关条件的章节外，本节的每一章都专门介绍在Ranorex Studio中构建数据驱动的测试的单独部分，并包含必要的分步说明。使用下面提供的示例解决方案将这些说明付诸实践。它带有准备好的测试套件和所需的模块。

[👉运行数据驱动的测试][1]一章中还提供了完整的示例解决方案。完成本章中所有步骤后，它将包含完成的项目。您可以将其用作参考。


**示例解决方案**
>主题：数据驱动测试简介                 
时间：30分钟            
[点击下载](https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleDataDrivenTesting.zip)    


**安装示例解决方案：**
1. 解压缩到计算机上的任何文件夹。

2. 启动 Ranorex Studio并打开解决方案文件RxSampleDataDrivenTesting.rxsln

**贴士**
>示例解决方案可用于Ranorex 8.0或更高版本。您必须同意8.2及更高版本的自动解决方案升级。

## 数据驱动测试的过程
为了让您入门，以下是有关数据驱动测试工作原理的快速概述：

一个测试用例包含录制模块组成的测试。录制模块，又包含了行动正在试运行期间进行，并且控件库项目执行这些动作上。

可以使这些动作和控件库项可变，并绑定到提供测试数据的外部数据源 。在测试运行期间，这些变量然后被提供来自数据源的值。测试是由数据驱动的 ; 因此，这是一个“数据驱动”测试。

像其他动作一样，您也可以使验证变量。这使您可以验证在数据驱动的测试期间输入的测试数据是否在AUT中产生了正确的结果，即实际结果是否与预期结果相对应。这是可选的，但非常有用。我们将在以下各章中构建的示例解决方案包括测试驱动的验证。

## 推荐知识
为了从本章的示例中获得最大收益，我们建议对以下材料有基本了解：

>**章节预览**                  
要遵循本章，您应该对Ranorex基础知识这一章有一定的了解，尤其是以下几章：           
👉[Ranorex录制器][2]              
👉[测试套件][3]                       
👉[动作][4]                
👉[仓库][5]                 
👉[测试验证][6]

---

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[定义变量👉][7]


[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/data-driven-testing/introduction/
[1]: .\executing-data-driven-tests.html
[2]: ..\\..\\ranorex-studio-fundamentals\ranorex-recorder\introduction.html
[3]: ..\\..\\ranorex-studio-fundamentals\test-suite\introduction.html
[4]: ..\\..\\ranorex-studio-fundamentals\actions\introduction.html
[5]: ..\\..\\ranorex-studio-fundamentals\repository\introduction.html
[6]: ..\\..\\ranorex-studio-fundamentals\test-validation\introduction.html
[7]: .\preparations-data-driven-testing.html