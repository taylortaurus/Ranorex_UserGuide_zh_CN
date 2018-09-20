# [译] GDI捕获功能

*原文地址 👉 [GDI capture feature][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-20*    

---

GDI捕获功能是Ranorex Spy其中的一个功能。可以从Ranorex Spy的树浏览器视图中的UI元素的上下文菜单访问该功能。

设置测试自动化脚本，识别被测应用程序（AUT）的UI元素。在某些情况下，Ranorex无法以适当的方式检测被测应用程序的所有UI元素（例如VB6，MFC，旧的Delphi版本）。这是GDI（图形设备接口）捕获列表功能发挥作用的地方。


**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [不基于GDI的UI元素标识](#xxx)
- [GDI捕获配置](#GDI捕获配置)
- [基于GUI的UI元素标识](#基于GUI的UI元素标识)
- [将进程添加到GDI捕获列表](#将进程添加到GDI捕获列表)
- [GDI捕获设置](#GDI捕获设置)

## 不基于GDI的UI元素标识

假设一个简单示例，你需要追踪和标识测试应用程序GUI之外的日历日期的。

![B4050-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4050-0000010.png)  
*不基于GDI的UI元素标识*

1. 启动Ranorex Spy并使用追踪功能
2. 在演示应用程序中标识日历日期25

### 结果

有时Ranorex不能从更大的环境中提取和识别不同的元素。当前结果如下图所示。

![B4050-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4050-0000020.png)  
*不基于GDI的UI元素标识结果*  

1. 看到RanoreXPath中没有显示日期，但是把完整的日历识别成UI元素
2. 看到Spy树浏览器视图中的UI元素的适配器未DateTime（即日历） 
3. 看到截图把完整的日历标识为UI元素，而不是25

![B4050-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4050-0000030.png)  
*树浏览器结果和路径编辑器*  

4. 看到Spy树浏览器视图中的UI元素的适配器未DateTime（即日历）
5. 看到路径编辑里UI元素的树视图

## GDI捕获配置

将uUI元素添加到GDI捕获列表中可以使Ranorex基于“RawText”适配器类来识别包含的UI元素。

![B4050-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4050-0000040.png)  
*GDI捕获配置*  

1. 验证选择Spy中的树浏览器视图
2. 选择要由GDI捕获功能处理的UI元素
3. 打开上下文菜单，然后单击`Add class name to GDI capture list`
4. 单击确定确认结果信息

## 基于GUI的UI元素标识

现在，我们重复前面的示例，以查看之前UI元素不可识别与现在的变化。

![B4050-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4050-0000010.png)  
*基于GDI的UI元素标识*  

1. 启动Ranorex Spy并使用追踪功能
2. 在演示应用程序中标识日历日期25

### 结果

Ranorex现在可以根据一种特殊的适配器类型`RawText`来识别以前封装的UI元素中的UI元素。  

![B4050-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4050-0000050.png)  
*基于GDI的UI元素标识结果*  

1. 看到RanoreXPath，已将日期25已被标识为UI元素
2. 在Spy的树浏览器视图中看到UI元素的适配器类型为`rawtext`
3. 看到屏幕截图，日期标识为UI元素，而不是之前标识的日历

![B4050-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4050-0000060.png)  
*基于GDI的UI元素标识的树浏览器和路径编辑器*  

4. 看到Spy中树浏览器的UI元素的适配器类型为`RawText`
5. 看到路径编辑器里UI元素视图


## 将进程添加到GDI捕获列表

除了复杂的UI元素之外，还可以将进程添加到GDI捕获列表中，以便能够跟踪和识别内部UI元素。

![B4050-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4050-0000070.png)  
*将进程添加到GDI捕获列表*  

1. 如果您未能在未知应用程序中识别UI元素，请选择该应用程序的父UI元素并打开上下文菜单
2. 单击`Add process name to GDI capture list`  

## GDI捕获设置

GDI设置可以通过Ranorex Spy中的设置访问。

![B4050-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4050-0000090.png)  
*GDI捕获设置*  

1. 点击Spy工具条上的`SETTINGS`
2. 选择常规设置对话框的`GDI capture settings`按钮

![B4050-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4050-0000100.png)  
*GDI捕获列表*  

GDI捕获列表显示了所有已注册的进程和所有已注册的UI元素类。



[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorex-spy/gdi-capture-feature/