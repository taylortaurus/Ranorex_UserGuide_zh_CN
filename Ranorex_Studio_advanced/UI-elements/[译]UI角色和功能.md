# [译] UI角色和功能

*原文地址 👉 [UI-roles & capabilities][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-20*    

---

追踪UI元素时，Ranorex指定此UI元素的角色和功能。Ranorex将每个UI元素映射到最适合的类型（即适配器类型）。如果没有合适的适配器类型，Ranorex将UI元素分类为“未知”。本章介绍和解释将UI元素映射到其角色和功能的概念。

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [UI元素映射流程](#UI元素映射流程)
- [技术无关的角色](#技术无关的角色)
- [角色特定的特征](#角色特定的特征)
- [指定技术的功能](#指定技术的功能)
- [功能和属性的可见性](#功能和属性的可见性)

## UI元素映射流程

本节将介绍为UI元素分配角色和功能的概念。请参阅下图，其中概述了整个过程。

![B5020-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5020-0000010.png)  
*UI元素角色和功能分配*

1. 技术无关的角色分配
    -  每个UI元素都与技术无关的角色匹配
    - 如果没有合适的角色可用，则选择Unknown
    - Ranorex从35+预定义角色中选择一个角色
2. 角色特定的特征
    - 存在直接从UI元素派生的指定的角色的特征（即属性，动作）
    - “常规”和“布局”包含角色的一组功能，与其类型无关
    - 与基本的UI元素相比，Dynamic包含扩展UI元素功能的属性
    - 每个角色还在具有角色名称的容器中托管一组角色属性
3. 属性/值对
    - “General”、“Layout”、“Dynamic”和“Role attributes”容器由一组属性/值对组成
    - 总之，存在643+属性/值对
4. 指定技术的功能
    - 另外，UI元素被分配一个或多个指定技术的功能
    - 在15个以上的类别中有167个以上的功能结构
    - 随着技术的发展，功能和类别将会增加
5. 属性/值对
    - 功能是通过属性/值对集定义的
    - 总之，存在643+属性/值对
  
## 技术无关的角色

下面显示的图像列出了一组众所周知的、常用的UI元素无关于技术的角色。Ranorex从35个预先定义的角色类型中选择一个角色。

![B5020-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5020-0000020.png)  
*UI元素中与技术无关的角色*  

### 角色分配示例

请参阅角色分配的简单示例。UI元素的作用很容易在Ranorex Spy和RanoreXPath中看到。

![B5020-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5020-0000030.png)  
*UI元素角色分析示例，部分1*

1. 在测试应用中带有性别选择的单选按钮
2. 在Ranorex录制器控件库中相应的控件库项名为`RdbFemale`
3. RanoreXPath中指定的UI元素角色(=适配器类型)

![B5020-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5020-0000040.png)  
*UI元素角色分析示例，部分2*

4. Ranorex Spy中的UI元素树浏览器视图，显示角色分配后的相应UI元素、
5. UI元素在Ranorex Spy中的角色名和元素名

## 角色特定的特征

与技术无关的角色是通过许多属性/值对和在不同容器中构造的操作来定义的。

![B5020-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5020-0000050.png)  
*角色特定的特征*  

1. 一般
    - 这个类别中的所有属性和操作都直接派生自ui元素(适配器类型)
    - 这个类别汇总了属性和动作，这些属性和动作可能起源于其他类别
2. 布局
    - 此类别包含所有引用UI元素的图形布局的属性
    - 这个类别的内容与技术无关 
3. 动态
    - 每当一个ui元素扩展其基本元素时，它就会实现放在这个类别中的属性和/或操作
4. 角色属性
    - 每个角色都引用具有角色名称的属性类别
    - 这个类别包含UI元素描述的所有指定角色的属性/值对和操作
    - 当前的示例概述了角色`RadioButton`的类别

### 角色特定特征的可见性

在Ranorex Spy中可以看到特定角色的特征(以及所有其他属性)。

![B5020-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5020-0000060.png)  
*Ranorex Spy中属性/值的可见性*

1. 属性概述:对UI元素的当前可用属性和已分配属性进行总结
2. 属性高级视图:详细显示在UI元素类别中组织的属性

## 指定技术的功能

如有必要，可以将一个或多个特定于技术的功能分配给UI元素。下面显示的图像显示了15种不同功能的结构。功能类别可以包含单个功能或最多100个功能。

![B5020-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5020-0000070.png)  
*特定技术的功能类别*  

### 功能分配示例

当前的示例概括了角色`RadioButton`的UI元素被分配了`Control`功能。如下图所示，`Control`功能是WinForms目录的一部分。

![B5020-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5020-0000080.png)  
*Control功能分配示例*  

1. Control功能:`capabilities Control`和`ControlNet11`是WinForms目录的一部分
2. 属性:功能控件包含四个属性/值对

## 功能和属性的可见性

功能和属性可以通过Ranorex Spy中的`Edit path weights`链接访问。

![B5020-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5020-0000090.png)  
*在Ranorex Spy中编辑路径权重的对话框*  

1. 在Ranorex Spy点击`Edit path weights`
2. 在显示的对话框中，单击链接`Show attribute overview`以显示所有功能和属性

![B5020-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B5020-0000100.png)  
*功能和属性概览*  

1. 功能
2. 功能中的属性结构


[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ui-elements/ui-roles-capabilities/

