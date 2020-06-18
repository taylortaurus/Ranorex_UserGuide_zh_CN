# [译] 追踪按钮

*原文地址 👉 [Track button][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-19*    

---

使用“Track”按钮手动标识和引用UI元素是一种快速且容易应用的方法。本节将展示如何进行此操作。

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [测试示例定义](#测试示例定义) 
- [追踪按钮](#追踪按钮)
- [追踪按钮的结果](#追踪按钮的结果)
- [追踪机制](#追踪机制)  

## 测试示例定义

为了解释通过跟踪按钮跟踪UI元素的概念，定义了一个简单的测试示例。所有必要的测试功能都是在演示应用程序的数据库工作环境中实现的。

![B3020-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TrackingUIEments/B3020-0000010.png)  
*追踪按钮--测试示例定义*  

1. 看到演示应用程序的Test database register选项卡
2. 测试示例的数据库工作环境

## 追踪按钮

跟踪按钮分布在Ranorex Studio的不同地方:

- Ranorex Studio录制器视图下方的控件库工具栏
- Ranorex Spy工具，如果Spy已经启动，或者控件库已经单独打开

**注意**  
> 在用户指南的相应章节中介绍和解释了Ranorex Spy的追踪按钮。目前主要对在Ranorex Studio和Ranorex录制器的追踪按钮功能进行介绍。

### 操作

1. 启动演示应用程序并选择测试数据库工作环境
2. 启动Ranorex Studio并使用有意义的名称打开一个新的测试解决方案

![B3030-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TrackingUIEments/B3030-0000010.png)  
*追踪按钮示例*  

3. 单击Ranorex Studio控件库工具栏中的`Track`按钮

![B3030-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TrackingUIEments/B3030-0000020.png)  
*追踪演示程序中的单选按钮*  

1. 一旦Studio在后台消失，追踪（单击）演示应用程序中的`Female radio button`  

**注意**  
> 激活track-button可以精确地跟踪一个UI元素。追踪功能到此结束。每个UI元素跟踪都需要单击它。

## 追踪按钮的结果

当一个ui元素被跟踪和识别时，追踪功能结束，Ranorex Studio将与最终的控件库一起再次出现。

![B3030-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TrackingUIEments/B3030-0000030.png)  
*追踪按钮-控件库*  

1. 控件库包含对UI-element单选按钮的跟踪和识别引用，并将控件库项命名为`RdbFemale`
2. 除了名称之外，还存储了一个惟一的标识符(所谓的RanoreXPath)。这个标识符指定GUI中对应的UI元素的位置，并帮助惟一地标识和描述ui元素

## 追踪机制

- 一旦激活（单击追踪按钮），追踪功能就可以精确地追踪和识别一个UI元素
- 追踪功能在追踪一个UI元素后自动结束
- 在追踪功能中按F12可以暂停追踪，因此，你可以追踪隐藏在下拉列表或菜单中的UI元素，这些下拉列表或菜单需要首先打开以进行追踪和识别

![B3030-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TrackingUIEments/B3030-0000040.png)  
*使用F12暂停追踪功能*  

1. 在追踪功能期间按F12可以从演示应用程序的下拉列表中追踪`Project Management`菜单项

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/tracking-ui-elements/track-button/
