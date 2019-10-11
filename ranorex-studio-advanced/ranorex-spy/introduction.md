# [译] Ranorex Spy

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月19日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年10月8日-green.svg?longCache=true&style=flat-square)

---

Ranorex Spy是Ranorex Studio的组件，它使探索和分析桌面，移动和Web应用程序的UI成为可能，以识别UI元素。间谍会捕获所有正在运行的应用程序（根据您的> 👉白名单），并在树视图中显示它们及其子元素。因此，它可以识别UI元素，对其进行标识，为它们分配一个RanoreXPath并最终使它们作为控件库项目可用于Ranorex Studio。

间谍软件可以作为独立版本使用，也可以从Ranorex Studio中获得。

在此页面上，您将找到如何启动Spy并使用其基本功能。


**本章导视**

- [相关章节](#相关章节)
- [启动RanorexSpy](#启动Ranorex Spy)
- [RanorexSpy布局](#Ranorex Spy布局)

## 相关章节
Ranorex Spy是一个高级主题，与RanoreXPath和UI元素的概念紧密相关。他们一起解释了Ranorex Studio中的UI元素标识如何工作。因此，我们建议您也学习这些章节。

> **章节预览**               
RanoreXPath的说明如下：                     
Ranorex Studio高级> [👉RanoreXPath][1]。

> **章节预览**               
UI元素的说明如下：              
Ranorex Studio高级>[👉UI元素][2]。

## 启动Ranorex Spy
Spy软件可以集成到Ranorex Studio中，也可以作为独立工具使用。

### **Integrated Spy**
a. 在Ranorex Studio工具栏中，单击 “Spy”图标。

b. 单击View>View Spy。

![B4010-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4010-0000010.png)


c. 在控件库中，单击所选控件库项目旁边的“EDIT IN SPY”。

![B4010-0000020](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4010-0000020.png)

### **单机版**
d. 从开始菜单中打开 Ranorex Spy。

![B4010-0000030](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4010-0000030.png)

**贴士**
>Ranorex Spy有32位和64位版本。在Ranorex Studio中运行Spy时，它使用与Ranorex Studio相同的位体系结构。运行独立版本时，由您决定选择哪种体系结构。
>
>我们建议始终使用与您的AUT具有相同位架构的所有Ranorex Studio工具。

## Ranorex Spy 布局
在下图中，您可以看到处于活动状态的“浏览器和结果”选项卡的独立间谍的布局。改为选择PATH EDITOR时，以绿色框起的区域会更改。这些区域作为页面[👉浏览器和结果][3]和[👉路径编辑器][4]的一部分单独说明。

红色区域已固定，下面将进一步说明。

![B4010-0000040](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4010-0000040.png)

1. 元素浏览器/控件库选择器（仅独立）
在元素浏览器和控件库之间切换。仅在独立的Spy中才可以加载控件库文件（.rxrep）。

2. 跟踪按钮和RanoreXPath字段
跟踪按钮使您可以跟踪，标识和添加新的UI元素。RanoreXPath字段显示元素的RanoreXpath并允许您对其进行编辑。

3. 在浏览器和结果屏幕与路径编辑器之间切换。
这些分别在页面[👉浏览器和结果][3]以及[👉路径编辑器][4]中进行说明。

4. UI元素树视图
此分层树结构表示所有正在运行的应用程序（取决于白名单设置）及其UI结构。

5. UI元素详细信息
在树中选择UI元素将在此部分中显示有关它的详细信息。

6. 图像导航区域
显示所选的UI元素，就像它在应用程序中一样，可用于在UI中导航。

### **元素浏览器/控件库选择器**
仅在独立版本的Spy中可用。使您可以在元素浏览器和控件库视图之间切换。

在控件库视图中，您可以加载和管理控件库文件（.rxrep）。当您要将控件库项目添加到无法使用Ranorex Studio的计算机上的控件库时，此功能特别有用。

![B4020-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000010.png)

控件库视图与Ranorex Studio中的视图相同，并且具有所有相同的功能。

![B4020-0000020](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000020.png)

>**章节预览**                            
管理控件库的说明                     
Ranorex Studio基础知识>[ 👉控件库][5]。

### ***追踪功能***
Ranorex Spy具有跟踪功能，可让您识别UI元素并将其添加到元素树中，然后从此处将它们添加到控件库中。

![B4020-0000030](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000030.png)

1. TRACK按钮和RanoreXPath字段：

- 跟踪按钮开始跟踪过程。
- RanoreXPath字段显示跟踪的UI元素的RanoreXPath


2. 根UI元素

- 您只能跟踪根元素中包含的UI元素。
- 在示例中，RxMainFrame（Ranorex Studio演示应用程序）是根元素，按钮RxButtonExit是被跟踪的UI元素。这意味着在Windows计算器中跟踪按钮是行不通的，因为它是一个单独的应用程序。如果根是整个端点，那么它将起作用。


### R**anoreXPath字段**

1. 编辑模式下的RanoreXPath字段
- 通常，RanoreXPath字段为白色，并显示树中当前所选元素的RanoreXPath。
- 当您单击该字段并按Enter时，它将更改为编辑模式。这由红色X，黄色背景和该字段下方的消息指示。
- 现在，您可以更改RanoreXPath并再次按Enter，元素树将显示与该路径匹配的所有元素。


2. 退出编辑模式

- 单击红色的X退出编辑模式。


### **工作环境选择器**
工作环境选择器使您可以在浏览器和结果显示器与路径编辑器之间切换。

![B4020-0000050](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000050.png)

---


&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[浏览器和结果显示器👉][6]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorex-spy/introduction/
[1]: ..\\..\\ranorex-studio-advanced\RanoreXPath/introduction.html
[2]: ..\\..\\ranorex-studio-advanced\UI-elements/introduction.html
[3]:..\\..\\ranorex-studio-advanced/ranorex-spy/ranorex-spy-functions.html
[4]:..\\..\\ranorex-studio-advanced/ranorex-spy/the-path-editor.html
[5]:..\\..\\ranorex-studio-fundamentals/repository/introduction.html
[6]: .\ranorex-spy-functions.html
