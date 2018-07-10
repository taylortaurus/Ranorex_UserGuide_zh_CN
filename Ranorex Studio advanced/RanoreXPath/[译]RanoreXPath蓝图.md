# [译] RanorexXPath 蓝图

*原文地址 👉 [RanoreXPath blueprint][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-7-6*  
*♋ update time : 2018-7-9*  

---

本章的目的是介绍和解释RanoreXPath的基本语法及其与Ranorex自动化测试的应用。本章的目标读者是对XPath或RanoreXPath知之甚少或根本不了解的初学者。本章概述了基础知识的基本概念。  


## 前言
---

RanoreXPath格式建立在W3C XPath语言格式之上。基本上，RanoreXPath是XPath格式的一个子集，并且在某些主题中，RanoreXPath扩展了XPath。与任何其他数学语法一样，RanoreXPath实现定义（扩展）语法和缩写语法。

虽然高级和有经验的用户通常使用缩写语法表示法，但这个介绍性章节主要使用定义和扩展的语言表示法。我们建议从本章开始学习RanoreXPath语法。当您取得进步并获得经验时，您可能会发现自己会自动应用缩写语言符号。

在必要和有用的情况下，我们提供语法选项和可能的缩写。

## UI元素描述
---

本节介绍和解释使用RanoreXPath表示法描述单个UI元素。

![B6010-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6010-0000010.png)    
*使用RanorexXPath指定一个按钮*  

1. **基本的RanoreXPath元素：** 一个基本的RanoreXPath包含三个元素-一个轴说明符、一个节点、零个或多个谓词来唯一标识和描述UI元素。  
2. RanoreXPath 使用角色按钮和谓词来描述演示应用程序的**退出**按钮，该谓词由唯一标识按钮的**属性--值**对组成

## 轴  

轴说明符指示UI元素的树表示中的导航方向。轴说明符的例子是/，/，..
、祖先等。稍后将在本节中更详细地描述它们。

## 角色（节点）  

- 正式的XPath语法将此格式部分定义为节点，而在Ranorex中，这称为角色（又称适配器类型）
- Ranorex使用引用的UI元素的角色作为RanoreXPath表示法中的主要描述标头
- 如果需要谓词来指定UI元素，则它嵌套在[]中

## 属性/值对（谓词）

- 属性值对可选地用于标识和描述XPath表示法中的UI元素
- 如有必要，可以组合两个或多个属性 - 值对以形成谓词
- 使用前面的@引入属性是一种约定
- 因此，属性值语法可能相当复杂 `@attribute ='value'` 是常见的惯例
- 属性--值对不仅应用 `=` 操作符。其他操作符将在后面介绍和解释
- 属性--值对不是标识UI元素的唯一选项。谓词可以由相当复杂的数学结构形成  

> **注意：**  
> Ranorex自动选择可用属性列表中最合适的属性--值对，以识别和描述UI元素。最合适的是指选择具有最高权重的属性--可由用户更改的属性。因此，可以影响UI元素的自动识别。

> **扩展阅读** 
> 在Ranorex Studio专家中介绍并解释了通过改变路径权重来映射动态UI元素的专家主题


## RanoreXPath结构  

本节介绍RanoreXPath的组成，以完全唯一地描述被测应用程序的GUI中的UI元素。 因此，RanoreXPath描述了Ranorex的抽象树表示中UI元素的位置。

### 基本概念

RanoreXPath结构的基本概念是简单地将UI元素描述链接在一起。

![B6010-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6010-0000020.png)  
*RanoreXPath结构*  

1. **根元素：** 定义当前UI元素树的根，即RanoreXPath格式的开头。
2. **路径：** 从根到节点：可选（零个或多个）分支元素，用于定义从根元素到指定节点元素的路径  
3. **节点元素：** 一个或多个UI元素，由当前的RanoreXPath格式标识  

### RanoreXPath示例介绍  

假设前一部分的示例--已在RanoreXPath语法中跟踪和描述了**退出**按钮。

![B6010-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6010-0000030.png)  
*RanoreXPath示例*  

1. 跟踪演示应用程序的**退出**  
2. 请参阅Ranorex自动生成的**RanoreXPath**格式  

![B6010-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6010-0000040.png)
*Ranorex Spy中的RanoreXPath示例*  

3. 查看UI元素树浏览器，其中UI元素以树状数据结构组织。
    -  根元素是演示应用程序的程序窗口（=form）
    -  它的控制名被定义为：`RxMainFrame`
    -  节点元素时退出按钮
    -  它的控制名被定义为：`RxButtonExit`
    -  没有额外的路径元素
4. 请参阅路径编辑器的RanoreXPath元素。 它们以分层形式表示RanoreXPath元素  

### 结果：

退出按钮的最终RanoreXPath格式如下所示：  

![B6010-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6010-0000050.png)  
*RanoreXPath格式示例结果*  

## RanoreXPath特性  

有两种主要方法可以使用和应用RanoreXPath格式。  

![B6010-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6010-0000060.png)  
*RanoreXPath主要应用*  

RanoreXPath描述UI元素的目的可以是识别单个UI元素也可以基于定义的分组特征识别一组UI元素。  

### 重点：  

独立于应用目的，RanoreXPath格式始终是：  

![B6010-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6010-0000070.png)  
*RanoreXPath原则*  

### 结果：

- 细节级别与灵活性对健壮性和执行速度有影响
- 一个非常详细的RanoreXPath导致声明不太健壮，但可能会加快执行时间
- 非常灵活的RanoreXPath变得更加强大，可以免受GUI架构的变化影响，在处理过程中变得更加耗时

## RanoreXPath健壮性  

Ranorex的一个突出特点是其针对图形用户界面中的动态变化的测试用例的稳健性。这种稳健性源于RanoreXPath定义的最大灵活性。  

RanoreXPath格式的自动生成试图在细节和灵活性之间找到一个很好的折衷方案。 这通常是通过尝试在路径格式中包含合适的容器元素来实现的。
**基本理念是基于通配符运算符。**  

### 示例定义

![B6010-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6010-0000080.png)  
*RanoreXPath健壮性示例定义*  

1. 使用Spy的**Track**功能  
2. 并在演示应用程序中跟踪测试数据库的Female单选按钮  

### 结果：

使用RanoreXPath，UI元素树浏览器和路径编辑器的项目树视图查看Ranorex Spy中的跟踪结果。  

![B6010-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6010-0000090.png)  
*RanoreXPath健壮性示例结果*  

1. **RanoreXPath格式：**  
    - 请参阅RanoreXPath格式及其组件，并将它们与Spy和路径编辑器中的视图进行比较。
2. **Spy中的UI元素树浏览器视图**  
    - 请参阅演示应用程序GUI的UI元素
    - 在UI元素树中构造了5个不同的UI元素
3. **路径编辑器**
    - 请参阅路径编辑器树视图中的RanoreXPath项
    - 从根到节点元素有7个RanoreXPath项
    - 它们共同构成了RanoreXPath格式  

### 详细的RanoreXPath格式

让我们仔细看看自动生成的RanoreXPath格式：

![B6010-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6010-0000100.png)  
*利用通配符使RanoreXPath健壮*  

4. **根元素 `RxMainFrame`:**  
    此UI元素表示被测应用程序（即演示应用程序）的程序窗口，是RanoreXPath规范的固定部分。 
5. **通配符：**  
    为使RanoreXPath格式尽可能灵活，Ranorex插入两个通配符 `/?`（可选）直到下一个固定的RanoreXPath标签项目。
6. **固定：**
    RanoreXPath项目 `RxTabStandard`Ranorex将此UI元素分类为RanoreXPathg格式的必要固定部分，以便能够稳健地识别节点UI元素。  
7. **通配符：**  
    接下来的两个RanoreXPath项再次使用 `/？` 通配符，以增加UI元素识别的灵活性。
8. 最后，**节点**元素 `rdbFemale` 是RanoreXPath格式的最终固定部分，用于成功且稳健的UI元素识别。  

### 总结：

- 对于通配符，即使底层GUI结构发生变化，Ranorex也能够无疑地识别UI元素
- 在当前示例中，Ranorex指定具有三（3）个固定UI元素的路径，这些元素对于单选按钮的UI元素标识是必不可少的
- 四(4)通配符为GUI更改提供了一种方法，并且不管这些变化如何，它们都是一个健壮的标识。
- 有三种不同的通配符运算符，将在下一节中介绍

## 通配符

RanoreXPath规范的灵活性基于通配符。 区分三种不同的通配符运算符：

|通配符|含义|描述|
|:--|:--:|:--|
|`/*`|任意一个|任何UI元素，恰好是一（1）个树级别|
|`/?`|任意一个可选|任何UI元素，正好是零（0）或一（1）树级别|
|`//`|任意一个后代|任意数量的树级别的任何UI元素|

### 当前示例总结

参考当前示例，让我们看一下通配符实现。

![B6010-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6010-0000110.png)  
*测试示例中通配符的应用*  

1. 可以看到UI元素 `RxTabControl` 被两个 `/?/?` 通配符替代。这就意味着下一个固定的RanoreXPath项目可以直接在UI元素的根级别或是一（1）、二（2）级别下定义，不用再进一步指定级别。
2. 可以看到UI元素 `grpGender` 被两个 `/?/?` 通配符替代。这就意味着下一个固定的RanoreXPath项目可以直接在UI元素的根级别或是一（1）、二（2）级别下定义，不用再进一步指定级别。  

因此，存在高达四（4）个级别的灵活性并且级别未进一步指定，这为GUI结构和内容的重大变化提供了空间。目标UI元素基于两个固定路径部分及其属性`controlname`找到。




[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorexpath/ranorexpath-blueprint/