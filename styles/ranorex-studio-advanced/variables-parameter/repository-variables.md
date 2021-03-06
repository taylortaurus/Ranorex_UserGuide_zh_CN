# [译] 控件库变量

*原文地址 👉 [Repository variables][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-18*    

---

除了文本或输入的数字字段可以是变量之外，任何用于交互的UI元素都可以由控件库变量自动执行。菜单项、列表项或单选按钮是这类UI元素的常见示例。这里引入了控件库变量的概念，用于列表项和单选按钮。


**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [控件库变量标识](#控件库变量标识)
- [定义控件库变量](#定义控件库变量)
- [默认变量值](#默认变量值)
- [控件库变量管理](#控件库变量管理)
- [应用控件库变量到radio按钮](#应用控件库变量到radio按钮)  

## 控件库变量标识

假设部门列表的选择项的下拉列表。选择项变量化，以使用数据集进行自动化。

### 涉及的动作项

![B2030-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2030-0000010.png)  
*控制下拉列表选择的操作项*

1. 动作#1表示单击部门选择项下拉列表的打开按钮
2. 动作#2表示从列表中选择项目管理部门项目，该选择是变量化的

### 控件库项  

--  
    ![B2030-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2030-0000020.png)
    *部门选项列表和相关的控件库项*  

3. 下拉列表的`Open`按钮是指控件库项`BtnDepartmentList`
4. 列表项选择指的是控件库常量项`ProjectManagement`，需要用控件库变量替换，用来数据驱动选择


### 标识控件库变量

固定的列表项的选择需要用存储库变量替换

![B1020-0000062](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B1020-0000062.png)  
*控件库变量标识*  

## 定义控件库变量

控件库项由它们的名称和它们在GUI中的位置定义。这个位置是通过RanoreXPath语法指定的。定义控件库变量意味着用变量替换RanoreXPath语法的一部分。然后，数据驱动的变量内容在运行时完成RanoreXPath规范，以使控件库项选择变量。

**章节预读**  
>  如果你不熟悉RanoreXPath的概念，推荐你先阅读在[RanoreXPath][1]章节

![B2030-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2030-0000030.png)  
*定义控件库变量*  

1. 选择负责相应UI元素交互的操作项（在当前示例中，操作＃2负责从部门列表中选择项目）
2. 打开上下文菜单并单击`Make repository item`变量

    ![B2030-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2030-0000040.png)  
    *控件库变量定义*  

3. 识别正确的属性(在当前示例中，从`ListItem`类别中选择`text`属性)，打开下拉列表并单击`new variable`
4. 为变量指定一个有意义的名称并单击OK
5. 可以看到控件库变量替代了先前UI元素属性的常量值
6. 单击路径编辑器窗口中的`APPLY`以结束指定控件库变量  

### 结果

你可以在存储库中找到相应控件库项的RanoreXPath被新的控件库变量替换的结果


![B2030-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2030-0000050.png)  
*控件库变量定义的结果*  

1. 在动作表和控件库中可以看到控件库项已经变量化
2. 发现修改后的RanoreXPath指定了包含了新的控件库变量`$LstDepartment`  


## 默认变量值

最初设置的值(即已记录的)将自动预先设置为默认变量值。在我们的示例中，因此将最初记录的“项目管理”部门的选择设置为默认值。默认值可以随意更改。

![B2030-0000052](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2030-0000052.png)  
*控件库变量默认值* 

**提示**
> 如果变量没有绑定到任何数据，则应用默认值。因此，谨慎地选择默认值可能很重要。建议为存储库变量定义适当的默认值。如果没有指定默认值，那么突出显示存储库中的ui元素将不起作用。  

## 控件库变量管理器

通过单击控件库工具栏中的`Variables`按钮来管理控件库变量

![B2030-0000130](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2030-0000130.png)  
*打开控件库变量管理器*  


**提示** 
> 所有当前控件库变量会显示在变量编辑器里

![B2030-0000140](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2030-0000140.png)  
*控件库变量编辑器*
 
1. 有变量名和默认值的控件库变量列表
2. 控件库变量工具条
    - 用来复制和粘贴的菜单
    - 直接新增变量按钮
    - 移除不在使用的变量（变量清理）
3. 变量提示
    -  `Variable in use`: 正在使用的变量，例如，被分配到控件库项的变量
    -  `Variable not in use`: 变量已被定义，但是没有分配到控件库项  

## 应用控件库变量到radio按钮

单选按钮变量化是控件库变量的常见应用。本节将展示如何做到这一点。

### Radio按钮动作

![B2030-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2030-0000060.png)  
*Radio按钮选择的动作*  

1. 动作1表示点击radio按钮`Male`
2. 动作2表示点击radio按钮`Female`

### Radio按钮控件库项

--
    ![B2030-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2030-0000070.png)  
    *Radio按钮控件库项*  

3. RdbMale控件库项引用了male单选按钮
4. RdbFemale控件库项引用了female单选按钮

### 创建单选按钮变量

![B2030-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2030-0000080.png)  
*创建单选按钮选择变量*  

1. 选择负责相应UI元素交互的操作项（在当前示例中，操作＃1负责单击男性单选按钮）
2. 打开上下文菜单，然后单击`Make repository item variable`

    ![B2030-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2030-0000090.png)  
    *单选按钮控件库变量定义*   

3. 从可用属性列表中识别适当的属性(在当前示例中，选择`controltext`属性)，打开下拉列表并单击`As new variable`
4. 为变量指定一个有意义的名称并单击OK
5. 可以看到控件库变量替代了先前UI元素属性的常量值

    ![B2030-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2030-0000100.png)  
    *控件库变量应用*  
6. 单击路径编辑器窗口中的APPLY以结束指定存储库变量

### 结果

你可以在控件库中找到相应控件库项的RanoreXPath被新的控件库变量部分替换的结果。


![B2030-0000120](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2030-0000120.png)  
*控件库变量创建结果*  

1. 可以看到在动作表和控件库中已变为变量的控件库项
2. 发现修改后的RanoreXPath指定了包含了新的控件库变量`$selGender`  

### 注意变量选择

必须仔细选择存储库变量的变量属性。在当前示例中选择controltext属性可能与测试数据项相关，但在不同情况下可能不合适。

**贴士**  
> 要使数据驱动的测试对本地化（其他语言）具有健壮性，建议使用其他属性，例如`ControlName`或其他

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/variables-parameter/repository-variables/
[1]: ..\\..\\RanoreXPath/introduction.html