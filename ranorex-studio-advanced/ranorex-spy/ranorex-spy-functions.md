# [译] 浏览器和结果显示器


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月19日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年10月9日-green.svg?longCache=true&style=flat-square)


---

如本章介绍页中所述，Ranorex Spy具有两种工作环境：浏览器和结果屏幕以及路径编辑器。在此页面上，您将找到前者的工作原理及其用途。

**本章导视**

- [元素树浏览器](#元素树浏览器)
- [元素树浏览器 功能](#元素树浏览器功能)
- [元素树浏览器上下文菜单](#元素树浏览器上下文菜单)
- [用户界面元素详细信息](#用户界面元素详细信息)
- [影像导航区](#影像导航区)


>**视频向导**                
视频“Spy功能”将引导您逐步了解本章中的信息。             
[立即观看](https://www.youtube.com/embed/HX81CztkxHo)

## 元素树浏览器
默认情况下，元素树浏览器位于工作环境的左侧。它是运行中的应用程序及其UI元素的分层表示。默认情况下，它显示在端点（即计算机）上运行并在Ranorex Studio中列入白名单的所有应用程序。但是，您也只能显示某个应用程序或节点。

树浏览器的功能将在下面进一步说明。

![B4020-0000060](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000060.png)

1. 元素树浏览器显示所有正在运行和列入白名单的应用程序。

2. 元素树浏览器仅显示该应用程序`RxMainFrame`，即Ranorex Studio演示应用程序。

## 元素树浏览器 功能

元素树浏览器上方的区域包含几个按钮和一个状态指示器。独立版和集成版Spy之间的按钮布局略有不同。区别在下面的标题中指出。

![B4020-0000070](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000070.png)


1. 浏览端点和端点（仅在独立的Spy中）

2. 刷新

3. 从快照加载...并另存为快照...

4. 高亮显示元素

5. 状态指示器

显示元素树浏览器的状态。三种状态是可能的：

![B4020-0000080](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000080.png)

a. 实时显示模式      
该树表示当前活动端点的应用程序。

b. 实时编辑模式              
您正在编辑当前活动端点的元素。

c. 快照模式              
该树是从Ranorex快照加载的，该快照表示端点应用程序的静态快照。

浏览端点和端点
- 浏览端点在活动端点（=自动化根目录）上显示所有当前正在运行并列入白名单的应用程序。
- 如果将树限制为特定的应用程序，请单击“ 浏览”端点以再次显示所有应用程序。
- 如果未定义端点，则自动化根为当前主机，即打开计算机Spy。
- 端点（仅在独立的Spy中可用）打开端点垫，您可以在其中选择要用作自动化根的端点。对于集成的间谍，您需要在Ranorex Studio的端点板中设置自动化根。

![B4020-0000100](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000100.png)               
*RanorexSpy端点视窗*

1. 单击工具栏中的“端点”按钮。

2. 端点视窗打开。

>**章节预览**             
端点说明              
Web和移动测试>[👉端点][1]。

### **刷新**
- 更新元素树以反映应用程序中的更改。

**从快照加载…和另存为快照…**
- 从快照加载使您可以打开现有的快照文件。
- 另存为快照会将当前选定的UI元素及其所有祖先和后代保存到快照文件中。

>**章节预览**               
Ranorex快照的解释如下              
Ranorex Studio高级> Ranorex Spy>[👉快照文件][2]。

### **高亮元素**
此功能与控件库工具栏中的功能相同。它用红色框突出显示了实际应用程序UI中的选定元素。自然，该应用程序必须正在运行才能正常工作。

![B4020-0000090](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000090.png)

1. 点击该高亮元素按键。

2. 该元素在应用程序中以红色框突出显示。

**注意**
>相应的应用程序必须正在运行并且在端点上可见，才能正常工作。

## 元素树浏览器上下文菜单

除了工具栏按钮之外，右键单击树中的元素还会弹出一个上下文菜单，其中提供了更多其他选项。

![B4020-0000110](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000110.png)                     
*UI元素树浏览器上下文菜单-第一部分*

1. 高亮显示元素
- 高亮显示应用程序中的元素。在上一主题中进行了解释。

2. 更新元素数据
- 刷新元素。在上一主题中进行了解释。

3. 将元素设置为根
- 使元素成为元素树浏览器的根。

1. 在树中，选择要设置为根的UI元素。

2. 在上下文菜单中，单击“将元素设置为根”。

3. 现在，树将元素作为根。

![B4020-0000140](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000140.png)

![B4020-0000120](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000120.png)    
*UI元素树浏览器上下文菜单-第二部分*

4. 添加到控件库

- 为该元素生成一个控件库项目，并将其添加到控件库中。
- 您可以仅添加所选元素，也可以添加元素及其所有子元素。
- 对于集成的Spy，将控件库项目添加到Ranorex Studio中当前处于活动状态的控件库中。
- 对于独立的Spy，控件库项目将添加到默认的Spy控件库或您已加载的控件库中。

![B4020-0000130](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000130.png)               
*UI元素树浏览器上下文菜单-第三部分*

5. 另存为快照...
将元素保存到快照文件。在上一主题中进行了解释。

6. 捕获屏幕截图

- 捕获元素在应用程序中显示的屏幕快照。对于基于图像的自动化很有用。
- 包含该元素的应用程序必须正在运行，并且该元素的路径有效。如有必要，请事先刷新元素树。
- 捕获后，将在图像编辑器中打开屏幕快照。
- 保存的屏幕截图还可用于代码中的图像比较，例如，用于查找和比较图像或基于图像的自动化。


## 用户界面元素详细信息
详细信息区域列出了所选UI元素的所有属性和属性。

![B4020-0000150](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000150.png)              
*UI元素详细信息区域*

1. 主适配器和元素名称

- 此外，还会显示有关UI元素在桌面上的大小和位置的信息。
- 值以像素为单位，并基于x / y坐标系。

2. 在概述和高级详细信息之间切换。

3. 显示详细信息的区域。

       
UI元素及其详细信息（即属性和属性）以及适配器的概念在以下内容中进行了解释：             
Ranorex Studio高级>[👉UI元素][3]。

4. 编辑路径权重...               
打开一个菜单，该菜单使您可以配置动态UI元素的映射。

>**章节预览**      
映射动态UI元素的说明如下                        
Ranorex Studio专家>[👉映射动态UI元素][4]。

## 影像导航区
图像导航区域显示所选元素所属的UI。您可以像在应用程序中一样浏览UI。单击图像中的UI元素时，将在树中将其选中。

1. 单击图像中的UI元素。

2. 选择了相应的树元素。

![B4020-0000160](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4020-0000160.png)


- 在图像导航器的顶部，您可以看到主要适配器类型和当前选定的UI元素的名称。
- 当您将鼠标移到图像中的UI元素上时，适配器类型和名称将相应更改。
- 在UI图像外部双击可切换到父元素的图像。

---

[👈简介][5]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[路径编辑器👉][6]





[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorex-spy/ranorex-spy-functions/
[1]: ..\\..\\web-mobile-testing/endpoints.html
[2]: ..\\..\\ranorex-studio-advanced/ranorex-spy/snapshot-files.html
[4]: ..\\..\\ranorex-studio-expert/mapping-dynamic-ui-elements.html
[3]: ..\\..\\UI-elements/introduction.html
[5]: .\introduction.html
[6]: ..\the-path-editor.html