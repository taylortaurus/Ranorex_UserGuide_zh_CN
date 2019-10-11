# [译] 工作环境和视图

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月26日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月4日-green.svg?longCache=true&style=flat-square)  


---

Ranorex Studio工作环境提供了一个管理测试解决方案及其所有组件的中心位置。本章介绍基本工作环境和默认视图。

**本章导视**

- [基本工作环境结构](#基本工作环境结构)
- [新增视图](#新增视图)
- [更改和选择视图](#更改和选择视图)

## 基本工作环境结构

Ranorex Studio提供了一个简单的工作环境，并根据共同的原则进行组织，例如分层组织。有关工作环境结构的介绍，请参阅下面的概述。

![A3030-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudio/A3030-0000010.png)
*基本的工作环境结构*

1. 项目视图

    - Ranorex Studio项目基于文件，并使用与Microsoft Visual Studio 2008/2010相同的项目文件格式
    - 项目视图显示当前与项目关联的所有文件和引用

2. 模块浏览器

    - 模块浏览器列出项目代码文件中的所有可用代码和录制模块。它还列出了项目模块组文件中的所有模块组
    - 此外，它还显示模块或模块组定义的所有变量
    - 此视图主要用于拖放自动化模块和模块组，以及在测试套件视图中重用模块和模块组

3. 文件视图
    -  双击项目视图中的文件或模块浏览器中的模块，以在Ranorex Studio的文件视图中打开关联文件
    -  此视图显示所有可用文件，例如测试套件视图，带有动作表和控件库的录制器视图，报告，代码模块等等
  
## 新增视图

有关所有可用视图的列表，请单击Ranorex Studio菜单栏中的`View`。

![A3030-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudio/A3030-0000020.png)  
*Studio菜单中的`View`菜单*  

**提示**  
> 用户指南的相应章节中描述了不同的视图。

## 更改和选择视图

使用Studio菜单栏的`View`菜单向工作环境添加视图。
要在活动视图之间切换，单击文件视图中相应的选项卡。

![A3030-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudio/A3030-0000030.png)  
*Studio文件视图中不同文件的可用选项卡*

1. 测试套件视图(*.rxtst)

    测试套件有这样的文件后缀`rxtst`=`R`anore`x` `t`est `s`ui`t`e 

2. 录制器视图(*.rxrec)

    录制器文件有这样的后缀`rxrec`=`R`anore`x` `Rec`order

3. 报告文件

    报告文件有这样的后缀`rxlog`=`R`anore`x` `Log`file

**贴士**  
>通过单击选项卡中文件名旁边的**[x]**，从工作环境中删除活动视图。

---
[👈创建一个新的测试项目][1]


[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/ranorex-studio/working-environments-views/

[1]:.\creating-new-test-project.html