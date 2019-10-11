# [译] 测试套件结构

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月6日-green.svg?longCache=true&style=flat-square)

---

**本章导视**


- [添加测试套件项目](#添加测试套件项目)
- [测试套件项目](#测试套件项目)
- [测试套件层次结构](#测试套件层次结构)

## 添加测试套件项目
有三种方法可以将项添加到测试套件中。

a.使用ADD按钮。

![A5020-0000011](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5020-0000011.png)


b.使用测试套件工作区中的上下文菜单。

![A5020-0000021](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5020-0000021.png)

c.从模块浏览器拖放,这仅适用于模块和模块组。

![A5020-0000031](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5020-0000031.png)

>**提示**   
>您只能在测试套件层次结构允许的情况下将项添加到测试套件中。如果无法在所需位置添加项目，则菜单中的项目将显示为灰色。本章末尾将介绍测试套件层次结构。





## 测试套件项目
在本节中，您将了解构成测试套件的项目。测试套件项可以分为两组，即结构项 和 测试动作项目。

结构项构成了测试的框架。

![A5020-0000041](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5020-0000041.png)

测试动作项包含测试期间要执行的动作。

![A5020-0000051](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5020-0000051.png)

### **测试套件**
test suit测试套件项用作根结构项。它包含所有其他项目，无法剪切，复制，粘贴或删除。它可以只包含其他结构项，如直接子项，即没有模块或模块组。

您可以在测试套件项中配置测试套件的全局参数和报告设置。通过菜单访问这些。

### **测试用例**
test case是一个结构化项目。 每个测试用例代表 测试套件的主要功能，例如向数据库添加条目。通过使用模块和模块组填充测试用例来构建测试用例。您还可以添加smart folder以测试案例以进一步组织它们。测试用例不能包含其他测试用例。

您可以通过其上下文菜单配置测试用例的错误行为，数据绑定和条件。

测试用例是测试报告成功计数器中计算的唯一项目 。

### **智能文件夹**
 smart folder像在文件夹层次结构中一样。您可以使用模块和模块组填充智智能文件夹是结构化项目。使用智能文件夹来组织测试套件，就能文件夹，但前提是智能文件夹是测试用例的子项。

您可以通过其上下文菜单配置智能文件夹的错误行为，数据绑定和条件。

### **Setup/teardown区域**
Setup和teardown区域是结构化项目。您可以将其中一个添加到测试套件项，测试用例和智能文件夹中。在设置区域将始终放置在开始的项目和的拆卸区域在年底。

要添加设Setup或teardown的区域：    

1. 右键单击所需的项目。 

2. 单击添加Setup或添加teardown。

![A5020-0000061](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5020-0000061.png)    
*添加Setup和teardown区域*

Setup区域始终在直接父项中的任何其他项之前执行。使用所需的模块和模块组填充设置区域，以使AUT达到运行以下模块所需的状态，例如启动AUT并登录。

teardown区域始终在其他所有区域之后执行，或者在直接父项目中发生错误时执行 。使用在测试运行后清理AUT所需的模块和模块组填充teardown区域，例如删除所有输入的数据并关闭AUT。

### **模块**
模块是测试数据项。它们包含在测试期间执行的动作。您可以将模块添加到除测试套件项目之外的所有结构项目以及不是测试用例子项的智能文件夹。

有两种类型的模块：

![A5020-0000071](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5020-0000071.png)   
*录制和代码模块*

1.录制模块
- 包含你用Ranorex Recoder所录制或者添加的动作和他的动作表

2.代码模块
- 包含在代码中的编程动作。


您可以通过其上下文菜单为模块配置数据绑定。您也可以将几个模块创建模块组，说明如下。

**提示**
>将模块添加到测试套件时，只需添加对它的引用。同样，当您从测试套件中删除模块时，您只删除该引用而不删除模块本身。

### **模块组**
模块组是测试数据项。使用它们对逻辑上属于一起的模块进行分组，例如通常一起出现的数据验证。您可以将模块组添加到除测试套件项目之外的所有结构项目以及不是测试用例子项的智能文件夹。

所有模块组都存储在单独的文件中。您可以在项目视图中的项目下找到此文件。默认情况下，它的命名为：[Project name].rxtmg


![A5020-0000081](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5020-0000081.png)   
*模块组文件*

添加模块组有两种方法：

直接分组

1. 在测试套件视图中，选择要分组的一个或多个模块。

2. 右键单击其中一个，然后单击“Group selected modules”。

3. 新创建的模块组将在模块组视图中打开。

将打开模块组视图，并选择新模块组。新模块组也出现在模块浏览器中。

![A5060-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5060-0000060.png)    
*使用直接分组创建模块组*


### **单独添加模块**
1. 在测试套件视图中，右键单击结构项以包含新模块组。

2. 单击add>new module group。将打开模块组视图，并选择新模块组。

![A5020-0000101](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5020-0000101.png)

3.从模块浏览器中拖放所需的模块至 模块组。
新模块组出现在模块浏览器中。您可以重命名模块组，并组织他们在文件夹中的模块组视图。

**提示**
>将模块组添加到测试套件时，只需添加对它的引用。同样，当您从测试套件中删除模块组时，您只删除该引用而不删除模块组本身。



## 测试套件层次结构
测试套件项目按层次结构组织。此层次结构控制可以添加或移动项目的位置，如下所示：

![A5020-0000111](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5020-0000111.png)    
*测试套件层次结构*

**提示**
>测试用例永远不会是另一个测试用例的子项。
当您将测试用例移动到另一个测试用例时，Ranorex会自动将其转换为智能文件夹。
智能文件夹只有在它是测试用例的子项时才能包含模块或模块组。

---
[👈测试套件][1]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[建立一个测试👉][2]

[0]:https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/test-suite/test-suite-structure-elements/
[1]:.\introduction.html
[2]:.\build-a-test.html