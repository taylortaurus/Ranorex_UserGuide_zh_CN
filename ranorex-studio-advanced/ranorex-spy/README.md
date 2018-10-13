# [译] Ranorex Spy

*原文地址 👉 [Ranorex Spy][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-19*    

---

Ranorex Spy独立于Ranorex Studio内部，或作为独立工具，提供探索和分析桌面和移动应用程序或测试网站所需的所有功能--包括其控件和UI元素。启动Ranorex Spy后，元素浏览器包含Windows桌面和移动设备上所有当前运行的应用程序。由于这种探索，你可以派生出每个识别的UI元素的相应RanoreXPath，并将其应用到Ranorex Studio中的自动化软件测试中。

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [必备知识](#必备知识)
- [启动Ranorex Spy](#启动Ranorex%20Spy)
- [Ranorex Spy工作环境](#Ranorex Spy工作环境)

## 必备知识

这个高级主题与RanoreXPath的概念和UI元素的主题密切相关。因此，在阅读本用户指南章节之前，我们建议你熟悉这两个主题。

> **章节预览**  
> 在 \> Ranorex Studio advanced \> 👉 [RanoreXPath][1]章节中详细介绍和解释了`RanoreXPath`的高级概念

> **章节预览**  
> 在 \> Ranorex Studio advanced \> 👉 [UI元素][2]章节中详细介绍和解释了`UI元素`的高级概念


## 启动Ranorex Spy

Ranorex Spy可以从Ranorex Studio开始，也可以作为Windows操作系统中的独立工具。

![B4010-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4010-0000010.png)  
*从Ranorex Studio中启动Ranorex Spy*  

- a. 在Studio工具栏上启动Ranorex Spy
- b. 使用Studio View菜单中对应的菜单项启动Ranorex Spy

![B4010-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4010-0000020.png)  
*在控件库中启动Ranorex Spy*  

- c. 使用控件库项所在行中的`EDIT IN SPY`按钮打开Ranorex Spy

![B4010-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4010-0000030.png)  
*启动Ranorex Spy独立版本*  

- d. 从Windows开始菜单打开Ranorex Spy独立的版本

**贴士**  
> Ranorex Spy目前可用作32位和64位版本。从Ranorex Studio内部启动时，将启动32位版本。当作为独立版本启动时，你可以选择不同架构。

## Ranorex Spy工作环境

Spy的工作环境看起来有点不同，具体取决于它的启动位置（Ranorex Studio内或是独立版本）。本节概述了基本工作环境及其6个主要领域。详细描述在随后的章节中进行，其中功能和应用程序通过示例介绍。

![B4010-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4010-0000040.png)  
*Ranorex Spy工作环境概览*  

1. 浏览/控件库选择器：Spy的独立版本能够加载和处理包含的控件库。在这里，你可以在两种模式之间切换
2. 追踪按钮和RanoreXPath信息：追踪按钮用于追踪，识别和添加RanoreXPath行，显示其唯一识别的新UI元素
3. 在UI元素树浏览器和路径编辑器之间切换：下面将详细介绍这两种工作环境
4. UI元素树浏览器视图：在图形用户界面中标识的UI元素的树状概览
5. UI元素详细信息：UI元素的详细信息，包括属性和图形信息
6. 图像导航区域：可以浏览UI元素


[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorex-spy/introduction/
[1]: ..\\RanoreXPath/introduction.html
[2]: ..\\UI-elements/introduction.html