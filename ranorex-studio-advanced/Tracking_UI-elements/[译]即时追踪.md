# [译] 即时追踪

*原文地址 👉 [Instant tracking][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-19*    

---

即时追踪主要用于快速添加多个存储库项，而无需单击Track按钮，然后反复移动到正在测试的当前应用程序。下面是如何应用这个快速跟踪功能。

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [测试示例定义](#测试示例定义)
- [即时追踪](#即时追踪)
- [追踪机制](#追踪机制)

## 测试示例定义

为了解释即时追踪的概念，定义了一个简单的测试示例。所有必要的测试功能都是在演示应用程序的数据库工作环境中实现的。目的是追踪和识别从下拉列表中选择的部门。

![B3040-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TrackingUIEments/B3040-0000010.png)  
*即时追踪-测试示例定义*  

1. 看到演示应用程序的Test database register选项卡
2. 测试示例的数据库工作环境

## 即时追踪

即时追踪是由简单的键盘快捷键`Ctrl` + `WIN`激活。看看它是如何工作的。

1. 启动Ranorex Studio并使用有意义的名称打开一个新的测试解决方案
2. 启动演示应用程序并选择测试数据库作为工作环境
3. 打开部门选择下拉列表

    ![B3040-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TrackingUIEments/B3040-0000020.png)  
    *即时追踪部门列表项*  

4. 将鼠标移到要追踪和标识的列表项上
5. 按下`Ctrl` + `WIN`来追踪选中的UI元素


## 追踪机制

- 如果Ranorex Studio或Ranorex Spy启动，或者打开了一个录制/控件库，即时追踪就会被激活
- 可以一次又一次地应用即时追踪，追踪所选的每个UI元素，并创建相应的控件库项


[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/tracking-ui-elements/instant-tracking/
