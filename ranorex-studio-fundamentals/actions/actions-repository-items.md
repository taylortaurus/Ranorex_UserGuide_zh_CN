# [译]动作和控件库项目
   

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月6日-green.svg?longCache=true&style=flat-square)


---

**本章导视**


- [动作和动作表](#动作和动作表)
- [UI元素和控件库项](#UI元素和控件库项)
- [动作和控件库项目](#动作和控件库项目)



## 动作和动作表
动作在录制器视图中的录制模块的动作表中进行管理。
![A6010-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6010-0000030.png)    
*Ranorex Studio中录制器视图的动作列表中的动作*

## UI元素和控件库项
控件库项是UI元素的表示。Ranorex使用控件库项来存储UI的结构并访问它。这样，Ranorex就可以对控件库项执行动作，从而对UI元素执行动作。控件库项目与“录制器”视图中控件库中的动作分开存储和管理。控件库以类似文件夹的层次结构组织。

例如，查看Ranorex演示应用程序的欢迎屏幕。每个UI元素由控件库项表示。请注意如何在控件库中组织项目。

![A6030-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6030-0000010.png)    
*UI元素和控件库项*

>**章节预览**             
>控件库的描述在>Ranorex Studio基础>👉[控件库][1]

## 动作和控件库项目
控件库项本身不做任何事情。只有当它们与动作相关联时才能实现其功能。虽然有一些动作无法链接到控件库项目，例如“Run”应用程序动作，但大多数动作可以并且在大多数情况下应该链接到控件库项目。试想一下，你有一个键序列，这不是链接到库项目，按键顺序总是在任何字段中输入成为关注焦点的时刻动作。这会使您的测试不可靠。

每一个动作告诉Ranorex做什么; 控件库项目告诉它在UI中的位置。

下图说明了鼠标单击动作和表示按钮的控件库项之间的链接。

![A6030-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6030-0000020.png)      
*动作和控件库项之间的链接*

1. 动作

- 动作＃4是鼠标单击UI元素，即`Submit`按钮。
- 此动作需要指向表示此按钮的控件库项的链接。

2. 控件库项目

- 控件库项`BtnSubmitUserName`表示UI元素，即`Submit`按钮。
- 每当对此按钮执行动作时，都会调用此控件库项。


3. 在动作和控件库项之间建立连接

- 动作和UI元素之间的链接是通过相应的控件库项建立的。
- 这在动作的第6列中指示，其中引用了控件库项。

---
[👈介绍][2]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[管理动作👉][3]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/actions/actions-repository-items/

[1]:..\\..\\ranorex-studio-fundamentals\repository\Introduction.html
[2]:.\introduction.html
[3]:.\managing-actions.html