# [译] 管理多个测试套件

*原文地址 👉 [Manage multiple test suites][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2019-9-6*    

---

**本章导视**
创建一个新的测试套件
剪切/复制/粘贴/删除/移动多个测试套件
设置测试序列
管理测试序列文件和参数
多个测试套件 - 功能列表


- [创建一个新的测试套件](#创建一个新的测试套件)
- [剪切/复制/粘贴/删除/移动多个测试套件](#剪切/复制/粘贴/删除/移动多个测试套件)
- [设置测试序列](#设置测试序列)
- [管理测试序列文件和参数](#管理测试序列文件和参数)
- [多个测试套件——功能列表](#多个测试套件——功能列表)
  
  >**视频向导**   
  >视频“管理多个测试套件”将引导您完成本章中的信息。   
  >[立即观看](https://www.youtube.com/embed/wUBTn6_JF_E)


## 创建一个新的测试套件

要将测试套件添加到现有项目，请按照以下说明操作：

![A5050-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5050-0000010.png)     
*添加新的测试套件*

1. 在Studio工具栏中，单击“添加测试套件”按钮。
2. 在出现的对话框中，确认该测试套件被选为模板。
3. 命名测试套件。
4. 点击Create。

### **结果**：
新的测试套件出现在项目视图中。通常，它也会在测试套件视图中自动打开。

![A05050-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5050-0000020.png)      
*新增测试套件*


1. 项目视图中的初始测试套件。
2. 项目视图中的新加入的测试套件。
3. 该测试套件选项卡的Ranorex工作室工具栏的下方。

新的测试套件文件也会出现在测试解决方案的Ranorex Studio Projects文件夹中。

![A05050-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5050-0000030.png)     
*Ranorex Studio Projects文件夹中的测试套件文件*

## 剪切/复制/粘贴/删除/移动多个测试套件

为确保项目的完整性，您无法剪切，复制或粘贴整个测试套件。但是，您可以删除并重命名测试套件。在项目视图中选择一个测试套件，然后打开上下文菜单以使用删除和重命名选项：

![A05050-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5050-0000040.png)      
*测试套件上下文菜单*

1. 剪切，复制，粘贴
- 无法剪切，复制或粘贴整个测试套件  。
- 同样，您无法将  整个测试套件移动到另一个项目。
2. 删除，重命名
- 可以删除测试套件。
- 测试套件可以重命名。

>**贴士**    
>虽然您无法移动整个测试套件，但您可以在测试套件之间移动测试套件内容。只需剪切/复制并粘贴所需的测试用例，智能文件夹，模块等。


## 设置测试序列

一旦项目包含至少两个测试套件，您就可以为测试套件指定序列。

1. 如果您的项目包含至少两个测试套件，则会在RUN按钮中添加一个上下文菜单。单击它以打开测试序列配置对话框。

![A05050-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5050-0000050.png)    
*多个测试套件 - 测试序列配置*

1. 启动项目选择
- 如果您有多个具有多个测试套件的项目，请选择要在此处配置的项目。
- 默认情况下，预先选择当前测试项目。
2. 使用左侧的顺序按钮  更改测试序列中测试套件的位置。

3. 使用ON / OFF按钮从测试运行中排除选定的测试套件。

![A05050-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5050-0000060.png)

4. 选择每个测试套件的运行配置。
>**章节预览**   
>Ranorex Studio基础知识>测试套件>⇢[执行测试套件][6]中描述了运行配置。

5. 单击“Run”按钮以启动指定的测试序列。


## 管理测试序列文件和参数
本节介绍存储测试序列的配置文件，并介绍如何将测试套件运行参数添加到此文件。

### **测试序列文件**
当项目包含至少两个测试套件时，将自动创建包含所有配置信息的测试序列文件，并将其添加到项目文件夹中。

![A05050-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5050-0000070.png)      
*测试序列文件存储位置*

1. 项目视图中的测试序列文件

2. 项目文件夹中的测试序列文件


>**贴士**    
>以.rxsqc为后缀的测试序列，可以使用任何文本编辑器进行编辑。


### **测试序列文件内容和语法**

![A05050-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5050-0000080.png)      
*测试序列文件内容*
1. 要打开测试序列文件，请双击它。它出现在自己的标签中。 
  
1.文本内容测试序列文件：
- `[ ]` 附上测试序列文件
- `{ }` 包含一个测试套件的所有配置
- 多个测试套件由`' , '`（JSON格式化语法）分隔
- 配置参数遵循语法 `"":""`
- 多个参数由`" , "`分隔

>**贴士**   
>您可以在测试序列文件打开时在配置对话框中配置测试序列。更改将实时反映在文件中。插入的命令行参数将保持不变。

### **添加命令行参数**
命令行参数可以添加到测试序列文件中，并在测试运行期间执行。

![A05050-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5050-0000090.png)     
*测试序列文件中的命令行参数*

1. 示例命令行参数 `/testcase`
- 命令行参数遵循先前引入的JSON语法定义
- 两个或多个参数必须用`' , ' `分隔
- 上面的示例`/testcase`使用名为`InsertName`参数值的测试用例调用命令行参数

>**章节预览**   
>Ranorex Studio基础知识>测试套件>⇢[在没有Ranorex Studio的情况下运行测试][7]，解释了测试套件的命令行参数。



>**暗示**   
虽然运行时环境中的命令行参数需要文件后缀（即.rxtst）文件参数，但这些后缀将在测试序列文件中被丢弃。

## 多个测试套件 - 功能列表
本节介绍Ranorex Studio 中多个测试套件的主要功能。它列出了通过多个测试套件可以做什么和不可以做什么。

### **传输测试套件内容**
可以将一个测试套件的内容传输（复制，移动）到同一项目或另一个项目的任何其他测试套件中。这意味着可以轻松地将测试用例，智能文件夹，Setup和teardown区域，模块等从一个测试套件复制或移动到另一个测试套件。

### **数据的完整性**
将测试套件内容复制或移动到另一个测试套件时，关于变量和数据绑定的数据完整性将保持不变。没有数据绑定丢失。

>**注意**
>如果满足以下任一条件，数据绑定将保持不变：
>- data绑定到全局参数，这些参数也可在目标测试套件中使用
>- 复制完整的数据环境。   
如果数据绑定到未复制的父测试用例或父智能文件夹，则数据绑定将丢失！

### **TestRail集成**
TestRail还可以为每个项目导出/同步多个测试套件。

>**章节预览**    
>在接口和连接> TestRail集成> ⇢[简介][8]中描述了与Ranorex的 TestRail集成。


### **Ranorex远程**
测试序列也可以从远程控制器上运行Ranorex代理。

>**章节预览**    
Ranorex Studio高级> Ranorex远程>⇢[简介][7]中介绍了Ranorex远程


---
[👈执行测试套件][6]















[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/test-suite/multiple-testsuites/

[6]: .\.\running-tests.html
[7]:.\\ranorex-studio-expert\\runtime-and-remote-execution.html
[8]:.\\interfaces-connectivity\\testrail-integration\\Introduction.html
