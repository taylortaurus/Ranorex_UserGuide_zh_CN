# [译] 控件库

*原文地址 👉 [Repository][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2019-9-9*    


---
存储库包含测试中使用的用户界面（UI）元素的表示，称为“存储库项目”。存储库项目以树状结构组织。每个项目都有一个RanoreXPath，它唯一地标识它，并允许Ranorex将项目与AUT的相应UI元素链接。

在本章中，您将学习如何创建，管理和构建存储库项目。您还将学习如何使用多个存储库以及特殊用例，例如嵌入存储库。

**本章导视**
- [UI元素](#UI元素)
- [存储库和存储库项](#存储库和存储库项)
- [存储库结构](#存储库结构)
- [存储库文件](#存储库文件)

## **UI元素**
Ranorex Studio测试包含与应用程序用户界面中的元素的一系列交互。UI元素包括按钮，选项卡，下拉菜单，文本字段等。Ranorex Studio将UI元素表示为控件库项目，以便与它们一起使用。

![A7010-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7010-0000010.png)       
*Ranorex Studio演示应用程序中的UI元素*

1. 简介注册标签
2. 欢迎文字标签 
3. 文本输入字段
4. 提交按钮
5. 重置链接
6. 退出按钮


## **控件库和控件库项**
控件库项目以类似树的结构在控件库中存储和管理。要访问控件库，请从项目视图中打开控件库文件。打开录制模块时，控件库文件也会自动打开。默认情况下，控件库显示在Ranorex Studio工作区的下半部分。

![A7010-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7010-0000020.png)   
*控件库和控件库项目*

1. 树状结构中的控件库项目

- 每个控件库项都有一个名称。默认情况下，此名称继承自AUT内部结构中调用UI元素的内容。
- 您可以根据需要重命名控件库项。
- 控件库项目在树状结构中的位置（即它所在的文件夹）建议相应UI元素在AUT中的位置。


2. 控件库项的路径

- 每个存储库项由其路径定义。
- 该路径源自AUT中UI元素的物理位置。
- 该路径遵循特殊语法RanoreXPath。


>**章节预览**   
在Ranorex Studio高级> 👉[RanoreXPath][1]中描述了RanoreXPath。

## **控件库结构**
控件库以树状结构组织，遵循AUT UI的内部结构。包含其他UI元素的UI元素在控件库中表示为文件夹，其中app文件夹充当顶级元素，而根文件夹充当子元素。

![A7010-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7010-0000030.png)     
*UI部分由控件库结构表示*

1. RxMainFrame
- RxMainFrame是一个app文件夹。它表示包含所有其他UI元素的应用程序的完整程序窗口。
- 在示例中，它唯一不包含任何其他项的直接子项是右下角的“Exit”按钮。
2. RxTabIntroduction
- RxTabIntroduction是一个有根文件夹。它代表“Introduction”选项卡的屏幕区域。
- 在示例中，它是RxMainFrame的直接子项，并包含“Introduction”选项卡中的所有UI元素。


## **控件库文件**
控件库的内容存储在控件库文件中。与其他Ranorex文件一样，您可以从项目视图或Windows中的项目文件夹中访问它。每个控件库文件还有两个子文件。

![A7010-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7010-0000040.png)     
*项目视图中的控件库文件和子文件*

这是图像的标题

1. 控件库文件
- 控件库文件的文件结尾.rxrep，代表Ranorex repository。
- 默认文件名是父测试解决方案（即Introduction）和的组合Repository。您可以根据自己的喜好重命名文件。


2. 存储库代码表示
- 带有结尾的文件.cs是C＃中存储库的代码表示。


3. 图像托管文件

- 带有结尾的文件.rximg托管链接到控件库项目的所有屏幕截图。
所有这些文件也可以在Windows的相应项目文件夹中找到。

![A7010-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7010-0000050.png)       
*控件库文件在项目的文件夹中*

### **添加控件库**
如果您的项目不包含控件库，则可以添加一个控件库。您还可以将👉多个控件库添加到项目中。

![A7010-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7010-0000060.png)

1. 在Studio工具栏中，单击 “Add repository”按钮。

2. 将打开一个对话框，其中预先选择了控件库模板。

3. 命名控件库。

4. 点击创建。



### **删除存储库**
1. 在项目视图中，选择主控件库文件（.rxrep）。

2. 按 DEL。

- 如果控件库不包含任何链接到操作的项目，则只需删除它。
- 如果至少有一个控件库项链接到某个操作，则会出现一个对话框通知您后果，您必须确认 缺失。


>**贴士**        
删除控件库时要小心。Ranorex Studio只能在当前打开的解决方案中找到控件库项目的引用。如果在另一个解决方案中使用控件库，则使用其控件库项的测试将会中断。

![A7010-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7010-0000070.png)           
*删除包含链接项的控件库时的确认对话框*


 ---
 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[控件库项目和动作👉][2]


[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/repository/introduction/
[1]:.\ranorex-studio-advanced\ranorexpath\introduction.html
[2]:.\repository-items-actions.html

