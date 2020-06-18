# [译] 路径编辑器


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月19日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年10月9日-green.svg?longCache=true&style=flat-square)


---

路径编辑器是Ranorex Spy中的第二个主要工作环境。在这里，您可以从元素树中指定和编辑已标识的UI元素的RanoreXPath。路径编辑器具有几个有用的功能，可以帮助您创建适合您需求的RanoreXPath。

在此页面上，您将找到路径编辑器的工作方式以及它提供的功能。

**本章导视**

- [访问路径编辑器](#访问路径编辑器)
- [找不到的元素](#找不到的元素)
- [锁定树步骤](#锁定树步骤)
- [路径编辑器的工作环境](#路径编辑器的工作环境)
- [编辑RanoreXPath](#编辑RanoreXPath)

>**视频向导**              
视频“路径编辑器”将引导您逐步了解本章中的信息。                
[立即观看](https://www.youtube.com/embed/a_IeBV5ebLY)

## 访问路径编辑器
您可以通过两种方式访问​​路径编辑器：从Spy中的工作环境选择器，或直接从打开的存储库中。

### **从Spy**
1. 在元素树中，选择一个UI元素。

2. 在工作环境选择器中，单击“ 路径编辑器”。

3. 出现路径编辑器工作环境，并且在路径树部分中突出显示了UI元素。

![B4030-0000020](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4030-0000020.png)

### **从存储库**
1. 在存储库中，选择一个存储库项目，然后…

a. … 单击 编辑间谍。

b. …右键单击它，然后单击“在间谍程序中编辑”。

![B4030-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4030-0000010.png)


## 找不到的元素
如上所述，在路径编辑器中打开UI元素时发生的常见错误消息是找不到该元素。这通常是因为包含UI元素的应用程序当前未运行。

### **初始情况**
1. 在存储库中，选择一个存储库项目。

2. 单击 EDIT IN SPY。

3. 路径编辑器将打开，并显示一条错误消息，并且路径树显示红色标记，表示找不到RanoreXPath指定的相应UI元素。

![B4030-0000030](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4030-0000030.png)

1. 红色符号表示找不到RanoreXPath指定的相应UI元素。

2. Spy状态栏中的错误消息，指示找不到UI元素。

### **解决方案**
1. 启动包含UI元素的应用程序。

2. 在路径编辑器中，单击 “Refresh”按钮以更新对UI元素的引用。

![B4030-0000040](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4030-0000040.png)

锁定树步骤
在路径编辑器中打开存储库项目时，其父存储库项目会限制您可以编辑RanoreXPath的哪一部分以及可以跟踪哪些UI元素。指定父级以上的RanoreXPath的任何组件都无法编辑。无法跟踪与父级相同或更高级别的UI元素。

这是因为在这些锁定级别进行的更改将影响其他存储库项目，并可能破坏现有的RanoreXPath。如果您需要更改父存储库项目或更高版本，请专门编辑这些项目。


![B4030-0000060](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4030-0000060.png)


1. EDIT IN SPY将打开存储库项目以在路径编辑器中进行编辑。

2. 您可以对RanoreXPath进行的更改受父存储库项的限制。

![B4030-0000070](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4030-0000070.png)

1. 浏览器和结果工作环境在元素树中显示存储库项目。

2. 存储库项目的父级已自动设置为根元素。此元素代表跟踪和编辑的限制。

3. 在路径编辑器中，锁定上方和包括根元素的所有元素以进行跟踪和编辑。

4. 可以跟踪和编辑根元素下的所有项目。

## 路径编辑器的工作环境
路径编辑器的工作环境由两个基本的Spy部分（红色框），两个特定的路径编辑器部分（绿色框）和一个状态指示器（橙色框）组成。

![B4030-0000050](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4030-0000050.png)


1. 跟踪按钮和RanoreXPath字段。在>简介中解释。

2. 工作环境选择器

3. 路径树          
以树结构显示UI元素的RanoreXPath的组件。             
刷新：更新树以反映相应应用程序中的更改。          
突出显示：突出显示相应应用程序中的UI元素。              
如果应用程序未运行，两者都会失败。

1. 属性规范             
列出可用的UI元素属性，运算符和值，以在RanoreXPath中使用。

5. 状态指示器            
指示当前RanoreXPath识别多少个UI元素。

## 编辑RanoreXPath

路径编辑器的主要应用是支持您编辑RanoreXPath，以便根据您的需要使其更通用或更具体。对路径进行实际更改的部分是RanoreXPath字段。我们已经在本章的简介中谈到了它，但是我们将在这里进行更详细的介绍。根据您是从元素树中编辑UI元素还是从存储库中已经存在的存储库项目，编辑会有所不同。

从元素树编辑UI元素时，路径编辑器的功能更像搜索，并且使您可以轻松查看给定的RanoreXPath将识别哪些UI元素。您可以认为它是不会影响测试的沙盒环境，除非您开始将已标识的UI元素添加到存储库中。

编辑现有存储库项目时，可以更改测试。因此，这样做时，RanoreXPath字段会稍微复杂一些，如下图所示：

![B4030-0000080](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4030-0000080.png)


1. 黄色主字段是您编辑RanoreXPath的位置。

2. 它下面的行显示了当前应用的（有效的）RanoreXPath规范，即开始进行更改之前的状态。

3. RanoreXPath的部分区域可能在黄色字段中显示为灰色。这表明它们已被锁定，无法进行编辑（请参阅上方的主题“锁定树步骤”）。

4. 该APPLY按钮取代了当前应用RanoreXPath（下行）与当前编辑RanoreXPath（黄色字段），关闭间谍并返回到Ranorex工作室，在那里你会看到反映在仓库项的新路径。

### **RanoreXPath语法支持**
RanoreXPath语法相当复杂。路径编辑器具有内置的语法支持，可简化编辑过程。

1. 编辑aRanoreXPath时，按 Ctrl + 空格键。

2. 将打开一个下拉列表，其中包含语义上可能的RanoreXPath语法部分。

![B4030-0000090](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4030-0000090.png)

### **选择/取消选择路径组件**
使用路径树，您可以轻松地在RanoreXPath中包含或排除特定组件。只需选择或取消选择它们，路径将自动更新。但是，有一些限制（请参阅下文）。

![B4030-0000120](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4030-0000120.png)


1. 复选框以选择/取消选择路径组件

请尝试以下操作以查看其效果：

1.选择一个组件。它包含在RanoreXPath中。

2.取消选择组件。它已从RanoreXPath中排除，但也会丢失信息，即适配器类型和属性。

3.重新选择组件。丢失的信息无法恢复；该组件现在是tabpage和radiobutton之间的任何UI元素的占位符。

![B4030-0000130](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4030-0000130.png)

如果以这种方式丢失信息，则可以重新跟踪UI元素或手动再次添加信息。

### **树上下文菜单**
路径树中组件的上下文菜单使您可以通过几种方式指定它们：

![B4030-0000140](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4030-0000140.png)


1. Optional（？）
 
将组件声明为可选，由？表示。在RanoreXPath之前的已修改组件。如果组件是可选的，则不需要使用该路径，即，如果未找到该组件，则该路径仍将起作用。当放置在适配器和属性之间时，两者都变为可选，这意味着如果两者（仅一个或两个都不能标识UI元素）都可以使用该路径。

2. Axis

Axis是关系运算符。它们允许您通过与其他UI元素的关系来选择UI元素。
可能的Axis：


|关键词|关系说明|
|:--|:--|
|child:|指当前节点的所有子节点|
|descendant-or-self:|指当前节点和节点本身的所有后代（子节点，孙子节点等）|
|ancestor:|指当前节点的所有祖先（父母，祖父母等）|
|self:|指当前节点|
|descendant:|指当前节点的所有后代（子，孙等）|
|parent:|指当前节点的父节点|
|ancestor-or-self:|指当前节点的所有祖先（父母，祖父母等）和当前节点本身|
|preceding-sibling:|指当前节点之前的所有兄弟节点|
|following-sibling:|指当前节点之后的所有兄弟节点|


> **章节预览**  
> 在 \> Ranorex Studio 高级教程 \> 👉 [RanoreXPath][1]章节中详细介绍和解释了`RanoreXPath`的高级概念

3. 节点名称

允许您为元素分配特定的适配器

> **章节预览**  
> 在 \> Ranorex Studio 高级教程 \> 👉 [UI元素][2]章节中详细介绍和解释了`UI元素`的高级概念

---

[👈浏览器和结果显示器][3]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[快照文件👉][4]




[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorex-spy/the-path-editor/
[1]: ..\\..\\ranorex-studio-advanced/ranorexpath/introduction.html
[2]: ..\\..\\ranorex-studio-advanced/ui-elements/introduction.html
[3]:.\ranorex-spy-functions.html
[4]:.\snapshot-files.html