# [译] 路径编辑器

*原文地址 👉 [The path editor][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-19*    

---

本节介绍和解释的路径编辑器--Ranorex Spy的重要组成部分。路径编辑器是指定和编辑追踪和识别的UI元素的RanoreXPath的地方。


**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [在Spy中启动路径编辑器](#在Spy中启动路径编辑器)
- [在Studio中启动路径编辑器](#在Studio中启动路径编辑器)
- [查找不到元素](#查找不到元素)
- [路径编辑器工作环境](#路径编辑器工作环境)
- [锁定树级别](#锁定树级别)
- [编辑指定的RanoreXPath](#编辑指定的RanoreXPath)
- [RanoreXPath语法支持](#RanoreXPath语法支持)
- [刷新树视图](#刷新树视图)
- [高亮元素](#高亮元素)
- [选择和删除路径元素](#选择和删除路径元素)
- [指定树元素](#指定树元素)


## 在Spy中启动路径编辑器

只需在工作环境选择器区域中选择路径编辑器，就可以从Spy中轻松访问路径编辑器。

![B4030-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4030-0000020.png)  
*在Spy中访问路径编辑器*  

1. 在浏览器树视图中选择一个UI元素
2. 在工作环境选择的路径编辑器链接
3. 在树视图部分中，选定UI元素查看已更改的路径

## 在Studio中启动路径编辑器

可以打开Ranorex Studio中的任一控件库项目，以在Spy中进行编辑。下图显示是如何做到这一点。

![B4030-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4030-0000010.png)  
*在Studio中访问路径编辑器*  

1. 在Ranorex Studio的控件库中选择一个控件库项
    - 单击控件项的`EDIT IN SPY`按钮，或者
    - 打开上下文菜单再点击`Edit in spy`

## 查找不到元素

如果你打开一个控件项，以在Spy中进行编辑，则可能存在Spy无法找到对应的UI元素的问题。如果托管UI元素的应用程序没有启动，就可能发生这种情况。

### 初始条件

![B4030-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4030-0000020.png)  

1. 在Ranorex Studio中选择一个控件库项
2. 单击`EDIT IN SPY`链接在SPY打开中的控件库项
3. 由于被测程序没有启动，可以看到Spy中元素树提示UI元素没有找到

**要点须知** 
1. 红色符号表示没有找到对应的UI元素
2. Spy窗口底部的状态消息将通知你没有找到UI元素

### 解决方案

![B4030-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4030-0000040.png)  
*UI元素没有找的的解决方案*  

1. 打开托管相应UI元素的应用程序
2. 单击`Refresh`以更新对UI元素的引用


## 路径编辑器工作环境

路径编辑器工作环境由4个基本区域和一个重要状态消息组成。

![B4030-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4030-0000050.png)  
*路径编辑器工作环境*  

1. 上面的黄色输入行表示路径编辑器的编辑行。这里是可以编辑RanoreXPath
2. 下方小字路径线显示当前应用的RanoreXPath。如果从Ranorex Studio打开，这一行将显示相应控件库项的当前有效的RanoreXPath。
3. 编辑行概括了的锁定部分(灰色)和可编辑部分(彩色)
4. `APPLY`按钮将当前应用的RanoreXPath(下一行)替换为当前编辑的RanoreXPath(上一行)，关闭Spy并返回Studio  

## RanoreXPath语法支持

路径编辑器为RanoreXPath规范提供了语法支持。看看它是如何工作的。  

![B4030-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4030-0000090.png)  
*路径编辑器的RanoreXPath语法支持*  

1. 在你写RanoreXPath时，需要帮助时，可以按下快捷键`Ctrl`+`Space`
2. 一个下拉列表将打开，其中有语义上可能的RanoreXPath语法部分供你选择

## 刷新树视图

通过单击工具栏中的Refresh按钮，可以刷新路径编辑器树视图部分中的树。当被测试的应用程序的图形用户界面(GUI)的体系结构发生变化时，刷新是必要且有用的。

![B4030-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4030-0000100.png)  
*路径编辑器刷新视图*  

1. 选择Spy的路径编辑器验证
2. 单击`Refresh`以刷新树视图

**贴士**  
> 如果未启动相应的测试应用程序，则刷新失败。

## 高亮元素

此功能高亮显示正在测试的应用程序中的相应UI元素。

![B4030-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4030-0000110.png)  
*高亮UI元素*  

1. 选择Spy的路径编辑器验证
2. 单击`Highlight `以高亮UI元素

**贴士**  
> 如果未启动相应的测试应用程序，则高亮失败。  

## 选择和删除路径元素

路径元素(即RanoreXPath部分)可以通过选择/取消路径编辑器树视图部分中树节点的相应复选框，轻松地从RanoreXPath中包含/排除。

![B4030-0000120](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4030-0000120.png)  
*选择/取消路径编辑器里树元素*  

1. 可以看到选择/取消树项的复选框

![B4030-0000130](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4030-0000130.png)  
*重选路径编辑器里的树元素*  

**要点须知** 
1. 选择一个树项
2. 取消一个树项
3. 重选一个树项

### 结果

- 相应的ui元素被排除，或者包含在RanoreXPath规范中
- 如果指定的树元素被取消选择并重新选择，Ranorex不一定检测它的初始适配器类型和选项属性值
- 你可能需要重新跟踪ui元素，或者手动指定适配器类型和属性/值对

## 指定树元素

任何树元素都可以直接在树视图部分中指定。本节将向你展示如何做到这一点！选择一个树项目并打开上下文菜单。

![B4030-0000140.](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexSpy/B4030-0000140.png)  
*路径编辑器指定树元素*  

1. 申明可选：将树元素声明为“可选”元素意味着Ranorex尝试指定RanoreXpath的元素，而不依赖于它们与可选树元素的关系
2. 关系运算符（轴运算符）：RanoreXPath规范中的元素不仅可以通过其在路径中的位置来定义，还可以通过其与其他（树）元素的关系来定义。可能的关系运算符如下：

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

3. 适配器类型规范：通过从上下文菜单中的选项列表中选择适配器，可以为树元素分配特定的适配器类型

> **章节预览**  
> 在 \> Ranorex Studio 高级教程 \> 👉 [RanoreXPath][2]章节中详细介绍和解释了`RanoreXPath`的高级概念


> **章节预览**  
> 在 \> Ranorex Studio 高级教程 \> 👉 [UI元素][2]章节中详细介绍和解释了`UI元素`的高级概念


[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorex-spy/the-path-editor/
[1]: ..\\..\\RanoreXPath/introduction.html
[2]: ..\\..\\UI-elements/introduction.html
