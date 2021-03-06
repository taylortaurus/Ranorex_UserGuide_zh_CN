# [译] 图像自动化初探

*原文地址 👉 [Image-based automation at a glance][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-11*  

---

在本章的介绍中，我们展示了一个默认自动化(即基于文本的自动化)失败的例子，因为它基于图形用户界面中UI元素的绝对和相对屏幕位置。本章介绍了基于图像的自动化的简单概念和简单的应用。

本章导视，章节内段落跳转推荐使用右上角的锚点！

- [测试实例准备](##测试实例准备)
- [基于图像的录制](##基于图像的录制)
- [测试结果](##基于图像的录制)
- [测试条件的改变](##基于图像的录制)
- [测试条件改变后的测试结果](##基于图像的录制)

## 测试实例准备

正如在本章的介绍中所示，测试用例基于一个日历视图，这个视图可以在初始测试记录和测试运行之间更改。

![B7010-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Image-basedAutomation/B7010-0000030.png)    
*基于图像的测试实例准备*  

1. 启动演示应用程序并选择基于图像的自动化作为工作环境
2. 在Ranorex Studio录制器技术选项中时选择即时录制

## 基于图像的录制

现在我们再次以基于图像的自动化模式录制上一个测试。

![B7020-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Image-basedAutomation/B7020-0000010.png)  
*在基于图像的自动化模式记录日历日期*

3. 通过勾选对应的复选框切换到基于图像的自动化
4. 在演示应用程序中录制(单击)当前日历视图的三个日期“24”、“25”和“26”
5. 这将生成一个包含三个对应动作项的动作表，其中UI元素已经以基于图像自动化模式记录

**提示**  
> 基于图像的自动化与基于文本的自动化（默认）在图形化方面也有所不同。
Ranorex录制器在录制时使用绿色帧(基于图像的自动化)而不是紫色帧(基于文本的自动化)描述标识的UI元素。  

![B7020-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Image-basedAutomation/B7020-0000020.png)  
*基于图像的自动化过程中绿色的UI元素检测帧*  

1. 基于文本的验证使用紫色帧验证元素
2. 记忆图像的验证使用绿色帧验证元素

## 测试结果

在使用录制状态运行的测试结果与默认的基于文本的自动化模式相同。

![B7020-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Image-basedAutomation/B7020-0000030.gif)  
*基于图像自动化的测试结果*

### 测试结果

- 测试报告显示了三个执行的测试项
- Ranorex录制器可以正确的标识先前录制的日历日期

## 测试条件的更改

同样地，假设测试条件在某种程度上发生了变化，日历视图在不同的月份发生变化，日期位于不同的位置，并观察基于图像的自动化的结果。

![B7010-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Image-basedAutomation/B7010-0000060.png)  
*更改的日历视图*  

1. 将日历视图从2018年1月更改为2018年2月

## 测试结果随测试条件的变化而变化

现在查看记录测试的测试结果，测试条件发生了变化，日历视图也发生了变化。

![B7020-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Image-basedAutomation/B7020-0000040.gif)  
*更改测试条件后的基于图像的测试结果*

### 测试结果

- 日期位于日历视图中的不同位置
- 然而，Ranorex正确地识别了之前选择的日期“24”、“25”和“26”!

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/image-based-automation/image-based-automation-glance/
