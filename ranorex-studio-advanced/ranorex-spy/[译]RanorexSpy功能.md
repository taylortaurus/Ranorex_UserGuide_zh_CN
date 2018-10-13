# [译] Ranorex Spy功能

*原文地址 👉 [Ranorex Spy functions][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-19*    

---

本章的目的是介绍和解释Ranorex Spy的各种功能和可能的应用。

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [元素控件库](#元素控件库)
- [Ranorex Spy追踪功能](#Ranorex%20Spy追踪功能)
- [Ranorex Spy工作环境选择器](#Ranorex%20Spy工作环境选择器)
- [元素树浏览器](#元素树浏览器)
- [元素树浏览器功能](#元素树浏览器功能)
- [元素树浏览器菜单](#元素树浏览器菜单)
- [UI元素细节](#UI元素细节)
- [图像导航区域](#图像导航区域)


## 元素控件库

在作为独立版本开始时，Ranorex Spy提供了处理和管理独立控件库的功能。管理控件库的选项表示为Ranorex Spy主工具栏中的元素控件库按钮。

![B4020-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000010.png)  
*Ranorex Spy的元素控件库选项*  

选中后，将显示一个存储库窗口，其中包含用于处理和管理控件库和控件库项目的所有功能，包括从磁盘位置加载控件库，将控件库导出到C＃，或VB.NET代码以及将控件库保存到磁盘位置。

![B4020-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000020.png)  
*Ranorex Spy元素控件工作环境*  

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 👉 [控件库][1]章节中详细介绍和解释控件库、管理和应用

## Ranorex Spy追踪功能

追踪功能允许追踪和识别UI元素，并将它们存储为当前控件库中的控件库项。

![B4020-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000030.png)  
*Ranorex Spy追踪功能*  

1. 追踪按钮和RanoreXPath标识符:

- 追踪按钮开始追踪UI元素
- RanoreXPath行显示所选（即追踪的）UI元素的唯一标识符

2. 根元素

- UI元素树浏览器的根元素限制了追踪功能
- 只能追踪根元素下面的UI元素
- 在该示例中，按钮`RxButtonExit`是当前选择（即追踪）的UI元素 

    ![B4020-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000040.png)  
    *RanoreXPath编辑行*  

3. 编辑模式下的RanoreXPath说明符行:

- 如果单击RanoreXPath行，它将更改为编辑模式
- 开头的红叉和黄色背景表示编辑模式
- 在编辑模式期间，禁用追踪

4. 结束编辑模式

- 要结束编辑模式并返回显示模式，请单击红色`X`.
- 叉叉消失，背景颜色再次变为白色

## Ranorex Spy工作环境选择器

工作环境选择器可以在Spy UI元素树浏览器和路径编辑器之间切换。

![B4020-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000050.png)  
*Ranorex Spy工作环境选择器*  

> **章节预览**  
> 在 \> Ranorex Studio 高级教程 \> Ranorex Spy \> 👉 [路径编辑器][2]章节中有详细的介绍和解释


## 元素树浏览器

元素树浏览器表示计算机桌面GUI的抽象表示。它包含桌面当前活动的所有应用程序中未指定的，未选择的所有ui元素。树浏览器还可以显示当前活动的桌面应用程序的已定义子集。

![B4020-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000060.png)  
*Ranorex Spy元素树浏览器*  

1. UI元素树浏览器显示当前所有桌面应用程序
2. UI元素树浏览器显示选择的桌面应用程序`RxMainFrame`的UI元素

## 元素树浏览器功能

本节介绍和说明UI元素树浏览器视图的各种功能。

![B4020-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000070.png)  
*元素树浏览器工具条*  

1. 浏览端点和端点
2. 刷新
3. 从快照加载和保存为快照…
4. 高亮元素
5. 状态指示器:显示UI元素树浏览器的状态，有已知三个不同的指标

![B4020-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000080.png)  
*Ranorex Spy元素浏览器状态*  

- a. 表示当前为显示模式
- b. 表示为编辑模式
- c. 表示为已加载快照文件后的还原模式

### 浏览端点&端点

- **浏览端点**显示当前在活动端点上运行的应用程序(设置为自动化根节点)
- 浏览端点提供默认的树视图，就像Ranorex Spy作为独立应用程序启动一样
- 果没有定义特定端点，则当前主机就是端点
- 如果尚未定义端点，端点将打开端点盘，该端点盘为空

![B4020-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000100.png)  
*Ranorex Spy端点菜单*  

1. 在工具条点击`Endpoints`按钮
2. 可以看到打开的端点管理器窗口

> **章节预览**  
> 在 \> 网页和移动测试 \> 👉 [端点][3]章节中有详细的介绍和解释

### 刷新

- 单击“刷新”按钮可刷新UI元素树以显示应用程序的当前状态

### 从快照加载和保存为快照

1. 第一个按钮功能打开现有的Ranorex快照文件
2. 第二个按钮功能将当前选定的UI元素，其所有祖先及其所有后代保存到Ranorex快照文件中

> **章节预览**  
> 在 \> Ranorex Studio 高级教程 \> Ranorex Spy \> 👉 [快照文件][4]章节中详细介绍和解释了相关内容

### 高亮元素

高亮功能的工作原理与控件库一章中介绍的类似。该功能通过周围的红色框架突出显示应用程序的相应UI元素。

![B4020-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000090.png)  
*Ranorex Spy高亮功能*  

1. 单击工具栏中的高亮显示元素按钮以激活高亮显示
2. 看到相应树元素的选定UI元素周围的红框显示


**贴士**  
> 请注意，托管UI元素的应用程序已在桌面上启动并可见

### 元素树浏览器菜单

除了UI元素树浏览器的工具栏功能之外，通过打开所选元素的上下文菜单，还有许多树元素功能可用，下面介绍这些功能。

![B4020-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000110.png)  
*UI元素树浏览器菜单--部分1*

1. 高亮显示元素：上一节介绍的功能
2. 更新元素数据：上一节中介绍的刷新功能
3. 将元素设置为根元素：该功能将选定的UI元素放在UI元素树浏览器的根位置

![B4020-0000140](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000140.png)  
*设置元素为根元素的功能*  

1. 选择要放在根位置的树的UI元素
2. 打开上下文菜单并单击`Set element as root`
3. 看到之前树元素设置为根元素了

![B4020-0000120](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000120.png)  
*UI元素树浏览器菜单--部分2*  

4. `添加到控件库`:将所选UI元素的引用添加到控件库中
- 选项是添加一个存储库项，或者添加一个包含所有子代的完整分支
- 如果Ranorex Spy是从Ranorex Studio内部启动的，那么控件将添加到当前的控件库中
- 如果Ranorex Spy作为独立工具启动，那么控件将被添加到Spy控件库中

![B4020-0000130](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000130.png)  
*UI元素树浏览器菜单--部分3*  

5. 保存为快照：上一节介绍的功能
6. 抓取快照：捕获当前UI元素的屏幕截图，以便在基于图像的验证中进一步使用

    - UI元素必须是有效的且是活动的;
    - 如果需要，进行刷新以使UI元素有效
    - 截图在Ranorex图像编辑器中打开
    - 截图默认以PNG文件格式存储在文件夹/Ranorex/控件库/中 
    - 保存的截图还可以用于代码中的图像比较，例如用于查找和比较图像或基于图像的自动化


## UI元素细节

UI元素详情区域列出了对应UI元素的所有属性。

![B4020-0000150](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000150.png)  
*UI元素详情区域*  

1. 主适配器和UI元素名称
    - 此外，还会显示关于桌面ui元素的大小和位置的信息
    - 值以像素为单位，在x-y坐标系中给出

2. 切换来显示UI元素属性的详细信息
3. 具有UI元素属性信息的窗口


> **章节预览**  
> 在 \> Ranorex Studio 高级教程 \> 👉 [UI元素][5]章节中详细介绍和解释了相关概念

4. 编辑路径权重：是关于动态UI元素映射的专家主题

> **章节预览**  
> 在 \> Ranorex Studio 专家教程 \> 👉 [映射动态UI元素][6]章节中详细介绍和解释了相关概念

## 图像导航区域

图像导航区域使得能够通过浏览所显示的（屏幕截图）图像来浏览树浏览器中的I元素。

![B4020-0000160](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4020-0000160.png)
*图像导航区域*  

1. 单击屏幕截图中的UI元素
2. 查看选定的对应树元素

**要点须知** 
1. 在图像导航器的顶部，你可以看到主适配器类型和当前选中的UI元素的名称
2. 通过将鼠标移动到当前选中元素的特定子元素上，你将看到适配器类型及其名称
3. 单击UI元素就是选择它
4. 双击所选元素外部即选择UI元素的父元素





[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorex-spy/ranorex-spy-functions/
[1]: ..\\..\\..\\ranorex-studio-fundamentals/repository/introduction.html
[2]: .\[译]路径编辑器.html
[3]: ..\\..\\..\\Web_and_mobile_testing/Endpoints/introduction.html
[4]: .\[译]快照文件.html
[5]: ..\\..\\UI-elements/introduction.html
[6]: ..\\..\\..\\ranorex-studio-expert/Mapping_dynamic_UI_elements/introduction.html