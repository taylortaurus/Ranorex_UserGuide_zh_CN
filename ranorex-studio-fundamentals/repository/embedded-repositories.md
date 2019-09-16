# [译] 嵌入控件库

*原文地址 👉 [Embed a repository][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2019-9-10*    

---

通常，控件库与录制模块分离。这种分离具有许多优点，容易在不同录制模块中重新使用控件库项目只是其中之一。

但是，有时您可能希望在存储模块中嵌入控件库。当您想要向其他人发送您制作的录制时，嵌入非常有用。没有它，你必须分别发送录制和控件库。由于这个原因，独立的Ranorex Recorder也总是创建带有嵌入式控件库的记录。

**本章导视**

- [嵌入控件库](#嵌入控件库)


## 嵌入控件库

1. 打开要在其中嵌入控件库的录制模块。

2. 在控件库工具栏中，单击当前分配的控件库的名称，然后单击“嵌入控件库”。如果您有多个控件库，则还可以先分配不同的控件库。


![A7092-0000011](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7092-0000011.png)

1. 项目视图中的控件库文件及其子文件。

2. 录制模块Recording1及其子文件。

3. 带有嵌入式控件库文件的录制模Recording1

>**贴士**          
您对具有嵌入式控件库的录制模块所做的任何更改仅限于该模块和该控件库。原始控件库不受影响，使用它的其他录制模块将继续工作。

---



[👈管理多个控件库][1]




[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/repository/embedded-repositories/
[1]:.\Manage-multiple-repositories.html