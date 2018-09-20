# UI元素

*原文地址 👉 [UI-elements][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-20*    

---

图形用户界面元素(即UI元素)是计算机屏幕上表示计算机内存储信息的可见图形元素。UI元素不仅表示存储的信息，还允许用户与软件交互。UI元素的常见示例包括窗口、文本字段、按钮、标签、列表和选择元素。

对于自动化软件测试，正确检测和识别被测试软件的UI元素是很重要的。因此，Ranorex Studio基于其UI元素检测的概念是一个基本概念，将在这里简要介绍。


**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [UI元素识别的概念](#UI元素识别的概念)
- [UI元素结构](#UI元素结构)

## UI元素识别的概念

UI元素的识别乍一看很容易。我们习惯于自己识别UI元素，并且知道如何使用它们。但深层的概念相当复杂。本节试图解释UI元素检测的基本原理。

让我们看一下Ranorex测试应用程序的介绍起始页面和一些现有的UI元素。


![B5010-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5010-0000010.png)  
*带有指定UI元素的演示应用程序*  

1. 演示程序的标题
2. 演示程序的主要菜单
3. 演示程序的选项卡
4. 文本标签显示欢迎信息
5. 文本区域用来输入名称
6. 文本链接重置欢迎信息
7. 退出按钮关闭应用程序

### 用户的观点

现在让我们在使用软件时采用用户的观点。这将有助于我们理解UI元素识别，从而了解Ranorex的功能。看一下特定的UI元素，一个文本输入字段。

![B5010-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5010-0000020.png)
*演示程序的文本输入区域*
 
**要点须知** 

- 为什么你知道红框UI元素是文本输入字段

#### 可能的答案

- 我在软件的用户指南中阅读了它
- 我从经验中知道
- 有人告诉我/给我看
- 由于提示“输入您的姓名”和“提交”按钮
- 我想这是一个文本输入字段，但我不知道

实际上，您无法查看软件内部以验证此特定UI元素是否真的是文本输入字段。而且您无法查看软件内部以查看其行为的定义，也无法查看其功能之一及其对软件的影响。但是，通过前面提到的一个或多个陈述，为什么您非常确定要面对文本输入字段，您已经创建了自己的“内部图片”或此UI元素的“内部表示”作为文本输入字段。

### 自动化UI元素识别

Ranorex通过两个步骤跟踪，识别和存储UI元素，下面将以简化的形式对其进行说明。

![B5010-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5010-0000030.png)  
*RanorexUI元素是被流程*  

1. UI元素是否在待测程序的GUI中
2. UI元素的内部表示

**要点须知**  

- 被测应用程序的GUI中UI元素由测试解决方案中的相应控件库项引用
- 每个存储库项都在树状数据结构中给出一个名称和一个位置，该结构抽象出被测应用程序的GUI结构
- Ranorex在最佳猜测方法上识别UI元素的类型，并将其映射到一组特定的角色和功能
- 另一方面，Ranorex为每个控件库项创建指定且唯一的标识符。此标识符反映了GUI元素在GUI中的位置，称为RanoreXPath


## UI元素结构

在分析测试中的应用程序期间，Ranorex识别UI元素并基于它们在GUI中的位置并基于它们彼此的相对位置来构建树状数据结构。以下示例可视化此概念：

![B5010-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5010-0000040.gif)  
*UI元素结构示例*  

构建结构意味着分析屏幕中结构元素中的UI元素（左图）的洋葱状嵌入，并导出适当的树状数据结构（右图）。

![B5010-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5010-0000080.png)  
*UI元素树示例*  

1. Form `RxMainFrame`
    
    - 此UI元素表示顶级UI元素，即演示应用程序窗口
    - UI元素几乎包含演示应用程序的所有其他UI元素（例外情况是上下文菜单，列表项以及通常在单独的树分支中组织的其他UI元素
    - 要包含在此元素中的UI元素的示例是“退出”按钮，主菜单或版权文本标签
2. TabPageList `RxTabControl`

    - 此UI元素表示选项卡容器，其中包含“简介”，“测试数据库”，“基于图像的自动化”，“UI元素测试区域”和“上传”
    - 在GUI分析期间，将从底层应用程序处理此UI元素的名称
3. TabPage `RxTabIntroduction`
    - 作为最终文本输入字段容器的选项卡名为“RxTabIntroduction”，当选择“简介”选项卡时，它在屏幕上可见
    - 此元素包含此选项卡寄存器中的所有UI元素
    - 该名称由底层应用程序处理
4. Text field `txtUsername`
    - 此UI元素表示名称的文本输入字段
    - 与“提交”按钮一起，文本标签“输入您的名字”和其他UI元素，此UI元素由上层容器托管
  
可以在Ranorex Spy的UI元素树视图中看到已识别的UI元素的分层树状结构：

![B5010-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5010-0000090.png)  
*Ranorex Spy的UI元素树浏览器视图示例*  



[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ui-elements/introduction/