# [译] 即时追踪

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月19日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月29日-green.svg?longCache=true&style=flat-square)

---
通过按Ctrl +  WIN可以进行即时跟踪  。这种跟踪方式对于从Ranorex Studio或Spy快速添加多个存储库项目特别有用，而无需重复使用“跟踪”按钮。在此页面上，您将了解其工作方式。

**本章导视**

- [测试示例定义](#测试示例定义)
- [即时追踪](#即时追踪)
- [追踪机制](#追踪机制)

**视频向导**
>视频“即时跟踪”将带您了解本章中的信息。               
[立即观看](https://www.youtube.com/embed/HFGmIa8O7gA)

## 测试示例定义
为了解释使用“跟踪”按钮进行跟踪，我们将使用Ranorex Studio演示应用程序的“测试”数据库。我们将跟踪的UI元素是“部门”下拉菜单中的列表元素之一。

![B3040-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B30/B3040-0000010.png)


1. 演示应用程序中的“测试数据库”选项卡。

2. 使用Department下拉菜单测试数据库的工作环境。

## 即时追踪

1. 启动 Ranorex Studio并创建一个新的空白解决方案。

2. 启动演示应用程序，然后单击“测试数据库”选项卡。

3. 点击该部门下拉菜单。

4. 将鼠标悬停在要跟踪的列表元素上。

5. 按 Ctrl + WIN跟踪列表元素。

![B3040-0000020](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B30/B3040-0000020.png)

## 追踪机制
- 如果启动了Ranorex Spy，或者在Ranorex Studio中打开了录制模块或存储库文件，则可以使用即时跟踪。
- 您可以一次跟踪任意数量的UI元素。您无需切换回Ranorex Studio或Spy。

---
[👈跟踪按钮][1]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/tracking-ui-elements/instant-tracking/
[1]:.\track-button.html
