# [译] 管理多个控件库

  

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月10日-green.svg?longCache=true&style=flat-square)

---

默认情况下，Ranorex Studio项目包含一个控件库文件，该文件自动用于每个新的录制模块。您可以管理模块在单个控件库中引用的所有控件库项，但也有充分的理由在单个项目中拥有多个控件库。本章解释了这些原因并描述了如何使用多个控件库。


**本章导视**


- [需要多个控件库的原因](#需要多个控件库的原因)
- [添加新控件库](#添加新控件库)
- [将控件库分配给模块](#将控件库分配给模块)





>**视频向导**    
视频“管理多个控件”将引导您完成本章中的信息：     
[立即观看](https://www.youtube.com/embed/_sa1xGcwf4s)


## 需要多个控件库的原因

### **测试不同的用户界面**

假设您的测试套件包含Web应用程序的测试用例和客户端应用程序用户界面的测试用例。在这种情况下，使用两个控件库是有意义的。一个包含Web应用程序的控件库项目，另一个包含客户端应用程序的控件库项目。您还可以使用简单文件夹将单个控件库中的两个应用程序的控件库项目分开，但使用两个控件库更方便，尤其是在团队中工作时。

### **模块化控件库**

以类似于录制和代码模块的方式模块化控件库是个好主意。例如，当您考虑具有主菜单，功能区或工具栏的客户端应用程序时，你可以创建小型可重用录制，以便在主菜单中单击UI元素，如文件> 打开 >处理打开文件对话框等。

所有这些可重复使用的模块都可以使用主菜单，主工具栏或类似工具，即共享控件。因此，最好还将它们建立在专门代表这些共享控件的控件库上。

### **同一个项目上有多个测试**

在单独处理项目时，单个控件库通常就足够了，通常不会成为问题。但是，在与他人合作时，这很快就会导致冲突。这可以通过使用多个控件库来规避。还要确保设置规则和职责，例如：谁可以重命名控件库项目？谁可以重组控件库？谁可以删除物品？

### **复杂点**
我们的一些客户拥有数千个控件库项目的测试。显而易见的是，将所有这些存储在一个控件库中会使其难以维护，更不用说这种控件库的文件大小了。随着测试变得越来越大，请考虑如何将控件库项目明智地划分到不同的控件库中，以保持其可维护性和高性能。

## 添加新控件库

![A7090-0000011](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7090-0000011.png)       
*添加新控件库*

1. 在Studio工具栏中，单击 “Add repository”按钮。

2. 控件库模板已预先选定。

3. 命名控件库。

4. 点击`Create`。


### **结果**：

- 添加了新的空控件库，可以在项目视图中看到。

![A7090-0000021](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7090-0000021.png)           
*添加了控件库*

1. 新添加的控件库文件，包含代码表示和图像托管文件。

2. 默认控件库。


## 将控件库分配给模块

一旦拥有多个控件库，就可以将它们分配给不同的录制模块。然后，您可以在录制中使用该控件库的控件库项。

### **目前已分配控件库**

打开录制模块时，当前分配的控件库将显示在控件库的工具栏中。

![A7090-0000031](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7090-0000031.png)          
*当前控件库分配*

1. `录制模块Recording1.rxrec......`

2. 把控件库IntroductionRepository分配给他们。


### **分配不同的控件库**

1. 在控件库工具栏中，单击当前分配的控件库。

2. 在下拉菜单中，单击要分配的控件库。


![A7090-0000041](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7090-0000041.png)              
*分配不同的控件库*

1. 当前分配的控件库。在这种情况下，它是默认控件库。

2. 另一个可用的控件库DatabaseTesting。

3. 如果录制模块包含链接到当前分配的控件库中的控件库项目的动作，则可以选择让Ranorex将这些控件库项目传输到新分配的控件库。

----

[👈使用单个控件库项表示多个元素][1]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[嵌入控件库👉][2]











[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/repository/multiple-repositories/
[1]:.\Represent-multiple-elements-with-a-single-repository-item.html
[2]:.\embedded-repositories.html