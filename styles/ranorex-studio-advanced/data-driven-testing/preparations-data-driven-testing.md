# [译] 数据驱动测试的准备

*原文地址 👉 [Preparations for data-driven testing][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-14*    

---

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [定义测试示例](#定义测试示例)
- [准备示例解决方案](#准备示例解决方案)
- [定义录制器变量](#定义录制器变量)
- [变量化列表项](#变量化列表项)
- [变量化Radio按钮](#变量化radio按钮)
- [变量化测试验证](#变量化测试验证)
- [准备好的变量概览](#准备好的变量概览)



## 定义测试示例

测试数据库是应用数据驱动测试的一个常见且非常适合的示例。因此，将使用Ranorex演示应用程序实现的一个小数据库来解释数据驱动测试的原理。

![B1020-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000010.png)  
*在Ranorex演示应用程序中测试数据库*  

1. 通过单击相应的选项卡激活测试数据库的工作环境

    ![B1020-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000020.png)  
    *在测试数据库中插入数据的原理*  

2. 将人员数据插入数据库表单并单击Add条目将人员添加到列表中

    ![B1020-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000030.png)  
    *测试示例，列出8人*  

3. 在测试示例中，一个接一个地将8个人添加到数据库中

4. 每次添加条目后，都会验证数据库计数器是否计算正确


## 准备示例解决方案  

对数据驱动测试的解释基于一个准备好的示例解决方案，这个示例解决方案将在本章中进一步开发，并且下载链接可以在本章的介绍中找到。👉 [数据驱动测试-介绍][1]  

![B1020-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000040.png)  
*示例解决方案的工作环境*

1. 项目文件视图：在文件夹中结构化的录制模块
2. 一个准备好的测试套件，用于待测的数据库测试场景

## 定义录制器变量

变量的定义是数据驱动测试设计的起始。本节演示如何用变量替换人名和年龄的常量文本值，然后用相应的测试数据填充这些变量。

![B1020-0000042](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000042.png)  
*录制模块变量示例*

**要点**

- 在我们的示例中，名字、姓氏和年龄的常量文本值将被变量替换
- Ranorex中的变量是以`$`开头，后面跟着变量名

**操作**

![B1020-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000050.png)  
*新增一个文本变量*

1. 在常量值旁打开下拉列表并单击`As new variable`

2. 为变量指定一个有意义的名称并点击`OK`确认

3. 看到绿色显示的变量名替换原来的常量值

### 定义所有录制器变量

![B1020-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000060.png)  


1. 变量$txtFirstName替换常量值“John”作为第一个名称

2. 变量$txtLastName替换了姓氏的常量值“Public”

3. 变量$intAge替换了年龄的常量值' 48 '

**进一步阅读**  
> [**录制器变量**][2]章节中详细介绍了变量和参数的概念，特别是录制器变量的定义  

## 变量化列表项  

除了文本输入字段可以是变量之外，任何用于交互的UI元素都可以由控件库变量自动执行。菜单项或列表项是这类UI元素的两个常见示例。本文引入了控件库变量的概念，用于列表项。

![B1020-0000062](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000062.png)  
*新增列表项变量*  

**要点**

- 常量“项目经理”作为一个部门类别被一个变量替代
- 所有列表项都包含在一个下拉列表中

**操作**

![B1020-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000070.png)  
*新增一个控件库变量*  

1. 选择与目标ui元素交互的操作项(即选择相应列表项的单击操作)

2. 打开上下文菜单并单击`Make repository item variable`

    ![B1020-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000080.png)  
    *分配一个控件库变量*   

3. 为变量指定一个有意义的名称并使用`OK`进行确认

4. 单击`APPLY`激活存储库变量定义

**结果**

![B1020-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000090.png)  
*定义列表项变量*  

1. 控件库变量`$lstDepartment`用于替换固定的部门选择  

**进一步阅读**  
> [**控件库变量**][3]章节中对控件库变量的定义和规范进行了详细的介绍和说明


## 变量化Radio按钮  

当前的测试示例概述了两个单选按钮，可选择性别。本节展示如何通过控件库变量使单选按钮选择变量化。  

![B1020-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000100.png)  
*变量化单选按钮*  

**要点**

- 解决方案基于控件库变量的原则
- 根据两个单选按钮的属性区分选择条件

![B2030-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B2030-0000110.png)  
*ControlText属性变量化单选按钮*  

当前示例的测试数据通过包含“male”和“female”作为值的数据项区分男性和女性。
因此，单选按钮属性`ControlText`用于区分选择。

1. 使用`ControlText`属性的选择`男性`单选按钮

2. 使用`ControlText`属性的选择`女性`单选按钮


**贴士**  
> 为了使数据驱动测试对本地化(其他语言)具有健壮性，建议使用其他属性，比如`ControlName`或其他属性

**操作**

![B1020-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000110.png)  
*创建一个控件库变量*  

1. 选择表示单选按钮的操作项，单击操作并打开上下文菜单

2. 单击`Make repository item variable`

![B1020-0000120](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000120.png)
*应用控件库变量*  

3. 为变量指定一个有意义的名称并使用`OK`进行确认

4. 单击`APPLY`激活存储库变量定义  


**结果**

![B1020-0000130](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000130.png)  
*单选按钮选择变量化*  

**进一步阅读**  
> [**控件库变量**][3]章节中对控件库变量的定义和规范进行了详细的介绍和说明

## 变量化测试验证  

正如测试定义中指定的，测试验证数据库计数器是否在每次插入后正确计算数据条目的数量。本节展示如何使测试验证变量为数据驱动测试做好准备。

![B1020-0000140](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000140.png)  
*测试验证变量化示例*  

**要点** 

- 数据库大小显示在演示应用程序中数据库列表的右上角
- 数据库大小更改后，相应的计数器会更新
- 数据库计数器将被一个变量替换

**操作**

![B2040-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B2040-0000040.png)  
*定义验证变量*  

1. 选择验证操作并打开匹配值的下拉列表，点击`As new variable`

2. 为变量指定一个有意义的名称并使用OK进行确认

3. 在操作列表中查看绿色的变量名`$intDBEntries`

**进一步阅读**  
> [**验证变量**][4]章节中对验证变量(即用变量替换匹配值)的定义和使用进行了详细的介绍和说明、

## 准备好的变量概览

在通过变量定义为数据驱动测试准备测试用例时，Ranorex Studio总是会显示你变量绑定的状态。

![B1020-0000160](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1020-0000160.png)  
*定义后但没有绑定的示例变量*

1. 测试套件视图显示已定义但未绑定的变量


[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/data-driven-testing/preparations-data-driven-testing/
[1]: .\introduction.html
[2]: ..\\..\\ranorex-studio-advanced/Variables_&_parameter/[译]录制器变量.html
[3]: ..\\..\\ranorex-studio-advanced/Variables_&_parameter/[译]控件库变量.html
[4]: ..\\..\\ranorex-studio-advanced/Variables_&_parameter/[译]验证变量.html

