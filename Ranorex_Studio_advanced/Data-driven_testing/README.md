# [译] 数据驱动测试

*原文地址 👉 [Ranorex Studio advanced][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*  
*♋ translate time : 2018-9-14*   
 
---

自动化测试是在许多迭代中使用不同的用户数据和不同的条件运行一个已定义的软件测试。为此，有必要将一个已定义的测试用例与一组创建不同测试用例迭代的测试数据相结合。基本原理称为数据驱动测试。在本主题中，将介绍与数据驱动测试相关的所有必要信息，并通过示例进行演示。

本章导视，章节内段落跳转推荐使用右上角的锚点！

- [解决方案示例](#解决方案示例)
- [数据驱动测试的概念](#数据驱动测试的概念)
- [Ranorex Testcase](#Ranorex Testcase)  
- [测试数据](#测试数据)  
- [变量和参数](#变量和参数)  
- [自动化测试验证](#自动化测试验证)  

## 解决方案示例 

通过一个示例解决方案解释了数据驱动测试的概念。这个解决方案可以在这里下载。该解决方案准备同时扩展到本用户指南中“数据驱动测试”一章的解释和说明。
一个完整的解决方案也可以下载。在最后一章的末尾可以找到相应的链接。

**我该怎么练习**  
> 主题: 介绍数据驱动测试  
> 时间: 30分钟以内  
> 下载: [点击下载示例][1]  

安装：

1. 将项目目录解压到计算机上的任一文件夹
2. 启动Ranorex Studio并打开解决方案文件RxDatabase.rxsln

**提示**
> 示例解决方案适用于Ranorex 8.0或更高版本。您需要统一将解决方案升级到8.2及更高版本。

## 数据驱动测试的概念

下面介绍的流程方案可视化了数据驱动测试的数据流和必要的流程步骤。

![B1010-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1010-0000010.png)  
*数据驱动测试流程方案*  


## Ranorex 测试用例

本用户指南的基础部分介绍并解释了构建测试用例的各种选项。如果您不熟悉Ranorex Studio的使用，录制一个测试脚本、录制测试模块、模块化录制以及在Ranorex测试套件中构建测试用例，我们建议您从基础部分开始阅读。

**进一步阅读**  
> 最重要的基本主题可以在左侧目录中`Ranorex Studio 基础教程`中找到  
> 👉 [Ranorex Studio(起始页)][2]  
> 👉 [Ranorex 录制器][3]  
> 👉 [测试套件][4]  


## 测试数据

创建测试数据是数据驱动测试的核心过程。本章将进一步介绍如何构建测试数据的选项。

**进一步阅读**  
> 数据的创建和绑定在[**数据和数据管理**][5]一章中详细介绍。

## 变量和参数  

变量和参数的概念将测试数据链接到Ranorex Studio的定义测试用例，并支持数据驱动测试。变量和参数是数据驱动测试的一个基本概念。这个概念需要与数据驱动测试方法一起理解。如果您不熟悉如何在Ranorex Studio中定义、使用和应用变量，我们建议您参考用户指南的相应章节。  


**进一步阅读**  
> [**变量和参数**][6]一章中详细介绍了变量和参数相关内容

## 自动化测试验证

数据驱动测试的关键原则是不断地验证基于测试数据的预期测试结果是否与自动测试运行期间创建的实际测试结果匹配。这个重要的概念将在本章后面的章节中介绍和解释。


[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/data-driven-testing/introduction/
[1]: https://www.ranorex.com/rx-media/rx-user-guide/v8.2/download/RxSampleDataDrivenTesting.zip
[2]: ..\\..\\..\\Ranorex_Studio_fundamentals/Ranorex_Studio/[译]RanorexStudio起始页.html
[3]: ..\\..\\..\\Ranorex_Studio_fundamentals/Ranorex_Recorder/index.html
[4]: ..\\..\\..\\Ranorex_Studio_fundamentals/Test_suite/index.html
[5]: .\[译]数据和数据的管理.html
[6]: ..\\Variables_&_parameter/index.html
