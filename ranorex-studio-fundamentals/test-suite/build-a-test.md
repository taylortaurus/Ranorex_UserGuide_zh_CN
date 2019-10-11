# [译] 建立一个测试

*原文地址 👉 [Build a test][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2019-9-5*    

---
在本章中，您将在前面的章节中应用您对测试套件的了解。为此，您将使用各种测试套件项构建一个简单的测试。


**本章导视**
- [下载示例解决方案](#下载示例解决方案)
- [定义测试](#定义测试)
- [查看录制模块](#查看录制模块)
- [组装测试](#组装测试)
- [运行测试](#运行测试)

>视频向导   
“手动构建Ranorex Studio测试套件”将引导您完成本章中的信息。   
[立即观看](https://www.youtube.com/embed/hE8kyP95TQA)


## 下载示例解决方案

要继续学习本教程，请从以下链接下载示例解决方案文件。

**示例解决方案** 
> 主题：分析录制   
> 时间：10min以内  
> 下载：[点我下载][1]  

安装示例解决方案：

1. 解压缩到计算机上的任何文件夹。

2. 启动 Ranorex Studio并打开解决方案文件RxDatabase.rxsln


**贴士** 
> 样本解决方案适用于Ranorex 8.0或更高版本。您必须同意8.2及更高版本的自动解决方案升级。

## 定义测试

在我们开始构建测试之前，我们需要定义它的功能。我们保持简单，所以我们的测试只会在数据库中添加一个条目，然后验证它是否已被添加。我们的AUT将是Ranorex演示应用程序。所需的步骤是：

1. 启动`Ranorex`演示应用程序。
2. 单击`test database`选项卡。
3. 在`First name`字段中输入名字。
4. 在`Last name`字段中输入姓氏。
5. 从`Department`拉列表中选择部门。
6. 在`Age`字段中输入年龄。
7. 从`Gender`框中选择性别。
8. 单击`Add Entry`。
9. 验证`Number of entries`已从0更改为1。
10. 退出Ranorex演示应用程序。

![A5070-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5070-0000010.gif)      
*动画测试定义*

## 查看录制模块

我们的示例解决方案已包含所需的录制模块。我们来看看他们。

![A5060-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5060-0000010.png)

这些模块分为两个文件夹。应用功能文件夹包含控制应用程序本身，即进入和离开Ranorex演示应用程序所需要的模块。数据库的功能文件夹包含有关添加到数据库中的条目的模块。

这些文件夹中的模块非常具体，您可以从名称中看到。它们每个都只包含测试定义中单个步骤所需的动作。以这种方式构建的模块更易于重用。这使您在构建测试时具有更大的灵活性。

## 组装测试

我们已经拥有了我们需要的一切，所以让我们开展业务并开始构建我们的测试。我们的项目中有一个测试套件RxDatabase.rxtst。它应该已经开放了。如果不是，只需在项目视图中双击该文件即可。

### **添加设置区域**
在测试套件视图中，您将看到测试套件基本上是空的，除了具有默认名称的单个测试用例。我们的测试定义列出了将AUT作为第一步的启动，这就是我们首先要添加的内容。启动AUT是包含在全局设置区域中的模块的完美示例，因为没有它，没有其他测试步骤可以工作。要添加全局设置区域：

1. 在测试套件视图中，右键单击测试套件，然后单击“Add setup”。

![A5060-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5060-0000020.png)    
*使用上下文菜单添加设置区域*

2. 从模块浏览器中，将模块StartAUT 拖到设置区域。除了启动演示应用程序之外，StartAUT模块还单击Test数据库选项卡，这是我们的测试定义中的第2步。

![A5060-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5060-0000030.png)


### **添加数据库测试**

测试定义中的步骤3到9表示向数据库添加条目并验证它。这是我们测试的核心，因此它应该有自己的测试用例。我们可以使用现有的测试用例，但我们首先给它一个更有意义的名称。

要重命名它：

1. 单击Test case，然后按F2。

2. 将其重命名为SimpleDatabaseTest，然后按 Enter键。

![A5060-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5060-0000040.png)    
*重命名测试用例*

现在我们可以用所需的模块填充测试用例。这些是测试定义顺序：InsertName，SelectDepartment，InsertAge，SelectGender，AddEntry和 ValidateEntries。您可以按照自己喜欢的顺序添加前四个模块，但AddEntry必须是倒数第二个，而ValidateEntries  必须是最后一个。

要添加模块：

1. 从模块浏览器中，将模块拖到测试用例中。

 - 您可以单独添加它们，也可以使用Ctrl + Click 一次选择多个模块。
 - 如果您在测试套件视图中放置了一个模块，只需将其拖动到正确的位置即可。

![A5060-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5060-0000050.png)

### **创建模块组**
模块InsertName，InsertAge，SelectGender和SelectDepartment都是同一过程的一部分：定义将添加到数据库的数据，换句话说，插入一个人。这就是为什么在模块组中组织它们是有意义的。这样，当您创建需要此过程的更多测试用例时，您不必反复添加所有四个模块。要将模块添加到模块组：

1. 在测试套件视图中，使用Ctrl +单击或Shift +单击选择四个模块。

2. 右键单击模块; 然后单击“ 组选定的模块”。

3. 新创建的模块组将在模块组视图中打开。

![A5060-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5060-0000060.png)      
*使用直接分组创建模块组*

4. 将模块组重命名为InsertPerson并关闭它。

5. 测试用例现在包含模块组InsertPerson，模块组也出现在模块浏览器中以供重用。

![A5060-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5060-0000070.png)

### **添加智能文件夹**
随着测试变得越来越大，越来越复杂，管理测试套件变得很困难。智能文件夹是一个有用的结构项，可以解决此问题。而不是使用50个模块填充测试用例，这些模块在逻辑上属于同一个测试，将智能文件夹添加到测试用例并组织其中的模块。智能文件夹还可以在测试执行期间轻松排除测试用例的特定部分。这正是我们将在我们的示例中使用智能文件夹的内容。我们可能并不总是希望执行验证，因此它将获得自己的智能文件夹。要将ValidateEntries添加到智能文件夹：

1. 右键单击测试用例SimpleDatabaseTest，然后单击添加>`New smart folder`。


![A5060-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5060-0000080.png)     
*添加智能文件夹*

2. 将ValidateEntries拖动到新的智能文件夹。

![A5060-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5060-0000090.png)      
*使用录制模块填充智能文件夹*

3. 将智能文件夹重命名为Validation。

![A5060-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5060-0000100.png)

**贴士**
>在Ranorex Studio基础知识>测试套件>👉[执行测试套件][2]中解释了从测试运行中排除项目。

添加teardown区域
我们的测试几乎完成了。我们只需要添加最后一步，退出Ranorex演示应用程序。这是应该在全局teardown区域中的步骤的完美示例，因为在此之后，没有其他测试动作可以执行。系统恢复到测试前的状态。通常，这还包括删除所有条目，但我们的数据库在退出时不保存任何条目，因此我们不需要包含此操作。要添加teardown区域：

1. 在测试套件视图中，右键单击测试套件，然后单击“添加teardown”。

![A5060-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5060-0000110.png)     
*添加teardown区域*

2. 从模块浏览器中,将模块ExitAUT拖动到teardown区域。

![A5060-0000120](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5060-0000120.png)


## 运行测试
恭喜，您刚刚在测试套件中构建了一个测试。您可以将本教程的基本原则应用于您将创建的任何其他测试。

这是您运行 测试的关键。我们将在下一章中介绍运行测试的详细信息和高级选项。现在，只需按下测试套件视图中的大RUN按钮，即可享受数据库测试！

**贴士**
>Ranorex Studio基础知识>测试套件>👉[执行测试套件][2]详细介绍了运行测试。

---
[👈测试套件结构][3]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[执行测试套件👉][2]











[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/test-suite/build-a-test/
[1]: https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleTestSuite.zip

[2]:.\running-tests.html
[3]:.\test-suite-structure-elements.html
