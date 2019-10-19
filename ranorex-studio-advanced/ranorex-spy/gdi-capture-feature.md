# [译] GDI捕获功能


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月20日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年10月9日-green.svg?longCache=true&style=flat-square)
 

---
在极少数情况下，Ranorex Studio无法正确识别AUT的UI元素。这适用于某些技术，例如VB6，MFC和较早的Delphi版本。在这些情况下，您可以使用GDI（图形设备界面）捕获功能正确识别这些元素。

GDI捕获功能是Ranorex Spy的一部分。您可以从元素树浏览器中的元素上下文菜单中访问它。

在此页面上，我们将通过Ranorex Studio演示应用程序中的一个简单示例来解释非GDI和GDI UI元素标识之间的区别：日历。

**本章导视**

- [默认的非GDI UI元素标识](#默认的非GDIUI元素标识)
- [启用GDI捕获](#启用GDI捕获)
- [将过程添加到GDI捕获列表](#将过程添加到GDI捕获列表)
- [GDI捕获设置](#GDI捕获设置)
 
>**视频向导**                  
视频“ GDI捕获功能”将引导您了解本章中的信息。                 
[立即观看](https://www.youtube.com/embed/frEDlUEE_iI)

## 默认的非GDI UI元素标识
我们要在演示应用程序中自动执行日历。为此，我们需要确定一个月中特定日期的UI元素。

让我们通过使用Spy中的track函数来标识元素：

1. 启动 Ranorex Spy，然后单击TRACK。

2. 在演示应用程序中，单击特定的日期，例如5月25日。

![B4050-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4050-0000010.png)


### 结果

![B4050-0000020](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4050-0000020.png)

1. 新UI元素的RanoreXPath显示的不是特定日期，而是整个日历。

2. 在元素树中，UI元素还具有适配器类型DateTime（即日历）。

3. UI元素的屏幕快照还显示了整个日历，而不仅仅是25个。


## 启用GDI捕获
由于默认的UI元素标识在这种情况下不起作用，因此我们需要启用GDI捕获。为此，我们将不正确的UI元素添加到GDI捕获列表中。在我们的情况下，这将使Ranorex Studio 基于RawText适配器类识别正确的UI元素。

1. 在元素树中，选择要由GDI捕获处理的UI元素。

2. 用鼠标右键单击它，然后单击添加类名GDI捕获列表。

3. 单击OK以确认信息对话框。

![B4050-0000040](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4050-0000040.png)

现在，我们可以再次跟踪UI元素。

1. 单击跟踪。

2. 单击日历中的特定日期，例如5月25日。

![B4050-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4050-0000010.png)


### 结果

UI元素的基础上正确识别RawText适配器。

![B4050-0000050](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4050-0000050.png)


1. 该RanoreXPath显示日期的某一天，而不是整个日历，已被确定。

2. 在元素树，UI元素具有适配器类型RawText。

3. 截图现在显示的具体日期，而不是整个日历的UI元素。


## 将过程添加到GDI捕获列表
我们建议只增加单个UI元素类的GDI捕获列表。但是，如果你需要添加整个过程（例如用于遗留原因），你可以在GDI捕捉设置，这将在下一个主题解释这样做。

## GDI捕获设置
GDI的拍摄设置显示所有添加过程和类名。这也是在那里你可以批量或正则表达式添加过程和类名。您可以从Ranorex Studio或间谍设置对话框访问GDI拍摄设置。

1. 单击设置...。

2. 在常规选项卡，单击GDI捕捉设置...。

![B4050-0000090](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4050-0000090.png)


3. GDI设置打开。

![B4050-0000100](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4050-0000100.png)


---

[👈快照文件][1]



[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorex-spy/gdi-capture-feature/
[1]:.\snapshot-files.html