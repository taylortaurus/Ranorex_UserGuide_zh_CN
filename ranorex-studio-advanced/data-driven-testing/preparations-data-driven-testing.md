# [译] 定义变量


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月14日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月27日-green.svg?longCache=true&style=flat-square)

---

在本章中，我们将首先定义数据驱动测试的步骤。然后，我们将定义此方案所需的变量。您还将了解如何在Ranorex Studio中管理变量。

变量是数据驱动测试的关键部分之一。它们是您要通过数据源或参数提供测试值的占位符。在Ranorex Studio中，我们区分三种类型的变量：动作变量，其子类型验证变量和控件库变量。


**本章导视**

- [定义测试示例](#定义测试示例)
- [定义动作变量](#定义动作变量)
- [定义控件库变量](#定义控件库变量)
- [定义验证变量](#定义验证变量)
- [默认值](#默认值)
- [管理变量](#管理变量)
- [定义变量概述](#定义变量概述)








**视频向导**
>截屏视频“定义变量”将带您了解本章中的信息。              
[立即观看](https://www.youtube.com/embed/tvoFKkebDKg)

## 定义测试示例
像往常一样，我们将使用Ranorex Studio演示应用程序作为示例。它具有我们将测试的数据库功能。测试数据库是数据驱动测试的常见现实应用。

该测试将包含以下步骤：

1. 启动演示应用程序。
2. 点击Test database选项卡。

![B1020-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000010.png)

2. 向数据库添加一个条目。

![B1020-0000020](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000020.png)

3. 重复如此，直到数据库中有8个条目…
4. 在输入了每个条目后，验证并确认该条目数更新正确。

![B1020-0000030](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000030.png)

5. 关闭演示应用程序。


### **示例解决方案和准备好的模块**
该[👉示例解决方案][1]已经包含了所有具有用于上述步骤的必要的动作的模块。它们以简单的测试套件进行组织。这将作为下一步的起点：用变量替换几个模块中的常量值。

![B1020-0000040](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000040.png)


1. 带有录制模块的模块浏览器，该录制模块在文件夹中构造，
2. 具有随时运行的数据库测试脚本的测试套件


## 定义动作变量
动作变量可以替换动作的组件或属性中的常量值，例如，键序列动作中的特定文本字符串。动作变量仅限于 在中定义的录制模块。

首先，我们将在用于在Demo App数据库中输入一个人的名字，姓氏和年龄的相应动作中替换常量文本值。

![B1020-0000042](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000042.png)

**注意**
>在Ranorex Studio中，变量名具有`$<variablename>`的格式，其中<变量名>不能以数字开头或包含任何特殊字符（下划线除外）。


用变量替换常量值：
1. 打开要更改的常数值的下拉列表，然后单击“As new variable”。
为变量

2. 命名这个变量，以便您可以简单得确定其占位符的值，然后单击“OK”。

3. 变量将以绿色显示在动作表中，以替换常量值。
![B1020-0000050](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000050.png)


4. 对姓（InsertName模块）和年龄（InsertAge模块）重复上述过程。

最终结果应如下所示：

![B1020-0000060](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000060.png)


1. 变量$txtFirstName将替换姓氏的常量值“John”

2. 变量$txtLastName将替换名字的常量值“Public”

3. 变量$intAge将替换年龄的常量值“48”

**注意**                
>动作变量只能在您定义它们的录制模块中使用。


## 定义控件库变量
除了使动作值可变之外，数据驱动的测试通常还涉及创建控件库变量。控件库变量用变量替换项目的RanoreXPath的特定部分（定义属性）。您可以通过这种方式使任何控件库项目变量。控件库变量在定义它们的控件库中以及引用此控件库的所有模块中都可用。

对于我们的示例，我们将使列表选择和单选按钮可变。这些是控件库项目，通常使它们具有可变性是有意义的，因为它们通常是具有多个选项的选择过程的一部分。

>**章节预览**                  
>有关RanoreXPath的更多信息，请转到                 
Ranorex Studio高级>  [👉RanoreXPath][2]

### **做一个变量选择列表**
在这里，我们将为“Department”列表选择变量创建控件库项目。在示例解决方案的SelectDepartment模块中，“click”动作链接到一个常量控件库项目，该项目指向列表中的“Project Management ”条目。在项目的RanoreXPath中，他的属性为@ text ='Project Management'

现在，我们将常量属性值Project Management替换为变量$lstDepartment，以便对将来的数据源指定的任何列表条目执行Click动作。

![B1020-0000062](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000062.png)


**注意**
>以后创建数据源时，我们需要确保部门选择的条目与列表中的条目完全相同，否则Ranorex Studio将无法识别UI元素。例如，没有条目IT，因此具有结果属性@ text ='IT'的控件库项目不会指向任何内容。


定义变量：
1. 右键单击第二个“click”动作，然后 选择“make repository item variable...”

![B1020-0000070](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000070.png)

2. Ranorex Spy打开时，文本属性的常量值已突出显示。单击其旁边的变量符号。

3. 为变量命名，以便您可以轻松识别它所引用的控件库项目，然后单击“OK”。

4. 在黄色栏中，单击“Apply”。

![B1020-0000080](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000080.png)


5. 现在，在控件库中，您可以在项目的RanoreXPath中看到该变量。

![B1020-0000090](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000090.png)


1. 控件库变量$lstDepartment用来替换选择department的常数值。


### **使单选按钮成为变量**
在这里，我们将为“Gender”选择变量创建控件库项目。在示例解决方案的SelectGender模块中，“click”动作链接到一个常量控件库项目，该项目指向Male的单选按钮。在项目的RanoreXPath中，他的属性为@ controlname ='rdbMale'。

现在，我们将使用变量（$selGender）替换此控件库项目的RanoreXPath中的常量属性值，以便对将来的数据源指定的任何Gender单选按钮执行Click动作。

![B1020-0000100](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000100.png)

**注意**
>稍后创建数据源时，我们需要确保性别选择的条目与两个单选按钮（即rdbMale和rdbFemale）各自的@controlname属性完全相同，否则Ranorex Studio将无法使用识别UI元素。仅包含Male和Female的数据源将不起作用，因为带有结果属性@ controlname ='Male'的控件库项目不会指向任何内容。


**贴士**
>使针对本地化（其他语言）的数据驱动测试变得强大，建议使用这样的的属性ControlName。
 

定义变量：

1. 右键单击 “click”动作，然后选择“Make repository item variable…” ...

![B1020-0000110](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000110.png)

2. Ranorex Spy打开时，文本属性的常量值已突出显示。单击其旁边的变量符号。
3. 为变量命名，以便您可以轻松识别其引用的控件库项目，然后单击“OK”。

4. 在黄色栏中，单击“Apply”。

![B1020-0000120](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000120.png)

1. 现在，在控件库中，您可以在项目的RanoreXPath中看到该变量。

![B1020-0000130](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000130.png)

1. 代表带有变量的“Gender”单选按钮选择的控件库项目$selGender

**注意**
>控件库变量可以在您在其中定义它们的控件库中以及使用此控件库的所有录制模块中使用。


## 定义验证变量
我们的示例测试包括一个步骤，该步骤验证添加条目时数据库计数器是否正确更新。为了使此验证有效，我们需要使其可变。

因此，我们将用一个变量替换ValidateEntries模块中验证动作的常量Match值。

![B1020-0000140](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000140.png)


**注意**
原则上，验证变量与动作变量相同。但是，由于“验证”动作比大多数其他动作更为复杂，因此我们将它们的变量分开对待，因此也分别解释了该过程。
 

定义变量：

1. 打开“match value”的下拉列表，然后单击“as new variable...”。

2. 将该变量命名，以便您可以轻松地识别出它是占位符的值，然后单击“OK”。

3. 变量将以绿色显示在动作表中，以替换常量值。

![B2040-0000040](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B20/B2040-0000040.png)


## 默认值
变量的默认值是没有数据源可用时使用的值。例如，从录制模块视图运行录制模块时就是这种情况。因此，您应始终确保定义一个有意义的默认值。

![B2020-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B20/B2020-0000010.png)

**注意**
>当用变量替换常量值时，原始常量值将自动用作默认值。


## 管理变量

要打开用于管理变量的对话框：

a. 对于动作/验证变量，打开定义它们的录制，然后单击VARIABLES…。

![B2020-0000020](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B20/B2020-0000020.png)

b. 对于控件库变量，请在控件库视图中单击Variables…。
![B2030-0000130](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B20/B2030-0000130.png)

变量管理对话框将打开：

![B2020-0000030](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B20/B2020-0000030.png)

1. 变量状态，名称和相应的默认值

2. 变量编辑器工具栏

- 用于将变量复制到剪贴板或从剪贴板复制粘贴的选项。
- 选择直接添加新变量。
- 选择删除未使用的变量（变量清除）。
- （仅适用于“动作/验证变量”对话框）用于将控件库变量复制到当前录制模块的选项，该变量在此成为动作变量。

3. 可变状态图例

- 变量在使用：变量使用，也就是说，它被分配到一个动作。不指示变量是否绑定/未绑定到数据源。
- （仅适用于 “动作/验证变量”对话框）从控件库中使用的变量：与先前相同，但用于从控件库复制的变量。
- 变量未使用：已定义变量，但未将其分配给动作项。不指示变量是否绑定/未绑定到数据源。


## 定义变量概述
现在，我们已经定义了数据驱动测试所需的所有变量。切换到测试套件视图后，现在可以看到每个模块定义的变量数量。请注意，它们仍未绑定，即尚未分配数据源。

在下一章中，我们将定义此数据源并将其分配给我们的测试用例。我们还将讨论用于管理数据源的选项。

![B1020-0000160](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1020-0000160.png)


1. 测试套件视图显示已定义但当前未绑定的变量

---

[👈简介][1]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[管理和分配数据源👉][3]


[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/data-driven-testing/preparations-data-driven-testing/
[1]: .\introduction.html
[2]: ..\\..\\ranorex-studio-advanced\ranorexpath\introdunction.html
[3]: .\data-data-management.html


