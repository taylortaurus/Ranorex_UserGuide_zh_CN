# [译] 快照文件

*原文地址 👉 [Snapshot files][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-19*    

---

Ranorex快照是在特定时间点被测试应用程序(AUT)的用户界面(UI)结构的文件表示。Ranorex快照捕获所有接口元素、它们的层次结构、值等。

它可以保存为单个文件。可以使用Ranorex Spy创建和查看Ranorex快照文件。文件扩展名是`.rxsnp`。

通常，Ranorex快照用于与Ranorex支持和技术销售团队共享应用程序UI的详细信息。

**本章导视，章节内段落跳转推荐使用右上角的锚点！**  

- [创建快照文件](#创建快照文件)
- [隐藏UI元素的快照](#隐藏UI元素的快照)
- [加载快照](#加载快照)

## 创建快照文件

本节介绍如何从UI中创建和保存简单的快照，它不包含隐藏的UI元素，如菜单、菜单项、上下文菜单、工具提示等。本文将向你介绍Ranorex快照的概念。

![B4040-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4040-0000010.png)  
*创建快照文件--部分1*  

1. 启动待测应用程序AUT（即演示应用）
2. 启动Ranorex Spy

![B4040-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4040-0000020.png)  
*创建快照文件--部分2*

3. 追踪测试应用程序中的UI元素(即演示应用程序中的Submit按钮)

![B4040-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4040-0000030.png)  
*创建快照文件--部分3*

4. 在Ranorex Spy点击`Save as snapshot`按钮
5. 选择一个保存位置并给快照文件取一个有意义的名称
6. 点击`Save`保存快照文件

**提示**  
> Ranorex在默认情况下将快照文件保存到`%USERPROFILE%RanorexSnapshot`

### 结果

进度指示器显示打包和保存快照的状态。最后，出现一条成功消息，可以使用`Close`确认。

![B4040-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4040-0000040.png)  
*创建快照文件--部分4*

**要点须知** 
快照通常包含相应的控件库项及其完整的祖先子树(Spy UI树浏览器)。你可以在高级设置和配置中更改此默认设置。

> **章节预览**  
> 在 \> Ranorex Studio 系统详情 \> 设置和配置 \>👉 [高级设置和配置][1]章节中详细介绍和解释相关概念

## 隐藏UI元素的快照

被测试应用程序的特定ui元素，如下拉菜单、弹出窗口、组合框等，只在鼠标单击后才可见，如果被测试应用程序失去焦点，通常会消失。这些元素通常不会自动包含在Ranorex快照中，因为它们在Ranorex Spy元素树的顶层作为单独的项出现。因此，对这些ui元素进行不同的快照。请看如下是如何做的。 

> **章节预览**  
> 在 \> Ranorex Studio 高级教程 \> 追踪UI元素 \>👉 [即时追踪][2]章节中详细介绍和解释了追踪隐藏的UI元素的相关概念  
> 在 \> Ranorex Studio 系统详情 \> 追踪UI元素 \>👉 [追踪按钮][3]章节中介绍了另外一种方法

### 快照隐藏的UI元素

![B4040-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4040-0000050.png)  
*创建隐藏UI元素的快照--部分1*  

1. 启动测试应用程序(AUT)(即演示应用程序)并切换到使用test database选项卡
2. 启动Ranorex Spy

![B4040-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4040-0000060.png)
*创建隐藏UI元素的快照--部分2* 

3. 选择隐藏的UI元素(即演示应用程序中的“项目管理”列表项)
4. 按`Ctrl+WIN`立即跟踪这个列表元素
5. Spy树浏览器中查看追踪到的UI元素

![B4040-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4040-0000070.png)  
*创建隐藏UI元素的快照--部分3*

6. 在执行其他操作之前——按下滚动条，创建先前跟踪的隐藏的UI元素及其所有控件树子元素的快照，并将其缓存到工作内存中。

**要点须知** 
1. 在工作内存中成功创建快照的信息。10个控件库项目被打包到一个快照中，该快照现在在Ranorex Spy中打开
2. 警告：通常会发生这种情况，如果你试图在不使用滚动的情况下创建隐藏UI元素的快照，创建的快照可能不完整。

**提示**  
> 按下滚动键后立即创建当前在Spy激活的控件库项及其完整的祖先子树的快照。

### 结果

在Ranorex Spy中打开一个快照。快照在Spy中的状态信息显而易见的。

![B4040-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4040-0000080.png)  
*创建隐藏UI元素的快照--部分4*  

### 保存快照

最后，需要将滚动创建的快照保存到物理存储内存(即磁盘、网络驱动器) 

![B4040-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4040-0000090.png)  
*保存隐藏UI元素的快照*  

1. 单击Spy工具栏中的`Save as snapshot`按钮，给它取个有意义的名称
2. 单击Save保存

### 结果

快照文件保存并提示成功信息

![B4040-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4040-0000100.png)  
*保存隐藏UI元素的快照文件*  

## 加载快照

本节演示如何将保存的快照加载到Ranorex Spy中。

![B4040-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4040-0000110.png)  
*加载快照文件--部分1*  

1. 启动Ranorex Spy，然后单击工具栏上的`Load from snapshot`
2. 选择文件夹和保存的快照文件
3. 点击打开

**提示**
> 如果没有更改，Ranorex将在%USERPROFILE%RanorexSnapshot中保存快照文件

### 结果

显而易见，快照被加载到Spy中。

![B4040-0000120](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4040-0000120.png)  
*加载快照文件--部分1*  

1. 看到状态信息中包含快照的创建日期



[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorex-spy/snapshot-files/
[1]: ..\\..\\..\\ranorex-studio-system-details/settings-configuration/[译]高级设置和配置.html
[2]: ..\\..\\Tracking_UI-elements/[译]即时追踪.html
[3]: ..\\..\\Tracking_UI-elements/[译]追踪按钮.html
