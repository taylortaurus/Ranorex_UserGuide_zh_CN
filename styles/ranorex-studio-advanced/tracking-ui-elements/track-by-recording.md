# [译] 录制追踪

*原文地址 👉 [Track by recording][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-19*    

---

通过录制进行跟踪是在测试用例录制期间跟踪UI元素的常规方法。虽然这个默认的跟踪方法已经在许多基础章节中使用过，但是为了完整起见，在这里解释一下。

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [测试示例定义](#测试示例定义)
- [录制追踪](#录制追踪)
- [录制追踪结果](#录制追踪结果)
- [追踪机制](#追踪机制)  

## 测试示例定义

为了解释通过录制跟踪UI元素的概念，定义了一个简单的测试示例。所有必要的测试功能都是在演示应用程序的数据库工作环境中实现的。

![B3020-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TrackingUIEments/B3020-0000010.png)  
*录制追踪--测试示例定义*  

1. 看到演示应用程序的Test database register选项卡
2. 测试示例的数据库工作环境

## 录制追踪

现在让我们看看如何通过录制跟踪是如何实际工作的。

### 操作

1. 启动演示应用程序并选择测试数据库工作环境
2. 启动Ranorex Studio并使用有意义的名称打开一个新的测试解决方案

    ![B3020-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TrackingUIEments/B3020-0000020.png)  
    *开始实时录制演示程序*  

3. 在Ranorex Studio的录制器视图中单击`RECORD`按钮
4. 选择`Instant records`记录已经启动的演示应用程序

    ![B3020-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TrackingUIEments/B3020-0000030.png)  
    *追东演示程序的一个单选按钮*  

5. 一旦Studio开始录制，单击演示程序中的`Female radio button`
6. 在录制器控制中心单击`STOP`并结束记录

## 录制追踪结果

录制结束后，打开Ranorex Studio工作环境，显示动作列表和当前控件库的录制器视图。  

![B3020-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TrackingUIEments/B3020-0000040.png)  
*录制追踪--动作列表*  

1. 鼠标单击操作，表示对引用控件库项`RdbFemale`的女性单选按钮的单击

![B3020-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TrackingUIEments/B3020-0000050.png)  
*录制追踪--控件库*  

1. 控件库包含对UI-element单选按钮的跟踪和识别引用，并将控件库项命名为`RdbFemale`
2. 除了名称之外，还存储了一个惟一的标识符(所谓的RanoreXPath)。这个标识符指定GUI中对应的UI元素的位置，并帮助惟一地标识和描述ui元素

## 追踪机制

- 在记录鼠标点击时，跟踪用户输入、鼠标移动(如果激活)和其他用户交互
- Ranorex标识相应的ui元素，并将它们以内部表示形式存储为控件库项
- 通常，每个UI元素只被控件库中的一个控件库项引用
- Ranorex可以识别用户界面元素是否多次使用，然后重用已识别的控件库项

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/tracking-ui-elements/track-by-recording/
