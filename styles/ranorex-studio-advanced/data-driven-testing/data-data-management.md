# [译] 数据和数据的管理

*原文地址 👉 [Data & data management][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-14*    

---

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [数据源管理](#数据源管理)
- [数据源分配](#数据源分配)
- [数据分配规则](#数据分配规则)
- [简单数据表](#简单数据表)
- [Excel数据连接器](#Excel数据连接器)
- [CSV数据连接器](#CSV数据连接器)
- [SQL数据连接器](#SQL数据连接器)
- [数据屏蔽选项](#数据屏蔽选项)
- [选择数据范围](#选择数据范围)

## 数据源管理

测试数据是基于测试套件集中管理的。测试解决方案的每个测试套件都拥有自己的测试数据集。在一个测试套件中管理的所有测试数据对于这个测试套件的任何测试用例都是可用的。本文介绍了测试数据的管理。

### 访问数据源管理器

![B1030-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000020.png)  
*范围测试数据管理器*

数据管理器可以在多个地方访问

- a. 在Ranorex Studio工具条点击`MANAGE DATA SOURCES`
- b. 在测试套件工具条点击`Data source`
- c. 在测试容器（测试用例，智能文件夹）的上下文彩蛋点击`Data source`  

### 数据源选项

在数据源管理器中添加新数据源、删除数据源和克隆测试数据源是数据源管理对话框中的基本操作。

![B1030-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000030.png)  
*基本数据源选项操作*  

1. 下拉选择新数据源，有四种不同的数据类型，下面将对它们进行解释
2. 通过单击Delete，可以在数据源管理器列表中选择和删除任何数据源

**提示**  
> 删除Excel、CSV或SQL数据源意味着删除到该数据源的内部链接，而不是数据源本身。物理存储的测试数据文件保持不变，并保持其存储位置不变  

**注意**  
> 删除一个简单的数据表意味着从物理上删除数据。数据将会丢失!原因：这种类型的数据直接存储在相应的测试套件(XML)文件中

3. 克隆数据源意味着克隆数据的引用。通过这个选项，可以为不同的测试用例或智能文件夹提供不同的数据子集

**提示** 
> 克隆一个简单的数据表意味着在相应测试套件的XML文件表示中复制其内容。

4. 可用的托管数据源

5. 数据源配置部分。根据数据类型的不同，需要进行各种配置设置以添加数据源，本节将详细解释不同数据类型。

## 数据源分配

虽然数据源是在测试套件中集中管理的，但是测试数据的分配是在测试用例和智能文件夹的基础上完成的。对于简单数据表，也可以在测试用例和智能文件夹中进行创建。

![B1030-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000040.png)  
*从测试用例和智能文件夹访问测试数据*  

1. 选择要分配给数据源的测试用例或智能文件夹

2. 点击`Data source`打开上下文菜单

![B1030-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000050.png)  

3. 打开下拉项获取数据源并选择

4. 在测试套件视图中查看测试用例或智能文件夹分配的数据源

## 数据分配规则

将数据源分配给测试用例和测试套件结构中的智能文件夹遵循一些需要记住的简单而重要的规则。

### 分配规则

|||
|:--|:--|
|规则1|每个数据源可以在垂直测试套件结构树中精确地分配一次|
|规则2|数据源只对结构中下级的测试套件起作用，对上级不起作用|
|规则3|数据源分配相互补充，而不是相互替代|

![B1030-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000060.png)  
*数据源分配示例*  

**要点须知**

1. CSV数据源被分配到智能文件夹A-1
2. Excel数据源被分配到智能文件夹A-2
3. 根据规则1~规则3，测试用例A中的测试模块没有分配数据源
4. 智能文件夹A-1的所有模块都能访问CSV数据
5. 参考规则2&规则3，智能文件夹A-2所有测试模块都能访问CSV数据和Excel数据
6. 参照规则2&规则3，智能文件夹A-2以下的任一测试用例或是智能文件夹中的所有测试模块都能访问CSV和Excel数据

![B1030-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000070.png)  
*数据源分配示例2*
 
**要点须知**

1. 所有的数据源都被分配到测试用例B和智能文件夹1下级。因此，相应的测试模块没有数据源可用
2. Excel数据源被分配到smart文件夹1-1。因此，该分支下的测试模块可以访问Excel数据
3. 智能文件夹1-2被分配了CSV数据，因此，它的相应测试模块可以访问这些
4. 智能文件夹1-2-1分配给Excel数据。根据规则#3，它的下级测试模块可以访问CSV和Excel数据
5. 智能文件夹1-3-1再次分配给Excel数据。因此，所有下级测试模块都可以访问Excel数据

## 简单数据表

对于小而简单的测试，基于简单的表数据创建测试数据是切实可用

![B1030-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000080.png)  
*创建简单数据表--部分1*  

1. 单击数据源管理器中的`New`按钮并单击`Simple data table`
2. 为数据连接器分配一个有意义的名称
3. 确认后点击OK

**要点须知** 
屏蔽数据项的选项将在本节末尾介绍和解释

![B1030-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000090.png)  
*创建简单数据表--部分2*

1. 使用表编辑器创建你选择的测试数据

![B1030-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000100.png)  
*创建简单数据表--部分3*

5. 完成后单击OK结束数据表创建过程

**要点须知** 
在本节的最后介绍和解释了选择数据表的数据范围的选项

## Excel数据连接器

使用以Excel文件格式存储的测试数据是一种选择。本节展示如何将这些测试数据添加和分配到数据驱动测试用例或智能文件夹。

**贴士** 

除了使用默认的Excel文件格式xlsx之外，还可以使用本机二进制文件格式xlsb。 Microsoft Office 2007支持此文件格式，并且比非二进制版本快得多。

![B1030-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000110.png)  
*创建Excel数据连接器*

1. 单击数据源管理器中的`New`按钮，并单击`Excel connector`
2. 配置完成后，确认OK  

### Excel连接器配置

1. 为连接器指定一个有意义的名称，并使用标准的Windows对话框选择文件位置

2. 如果应用版本控制，则必须检查此选项。否则，你可能无法访问测试数据。即使没有，也强烈建议将测试文件复制到你的测试环境中。

3. 选择工作表

    - 如果测试数据分布在Excel文件中的两个或多个表中，则可以在此指定受影响测试数据的位置
    - 此外，可以在这里指定子集的范围
    - 在启动时不加载工作表意味着没有确定行数，因此不能在测试套件中显示

4. 屏蔽数据项的选项将在本节末尾介绍和解释

**贴士**
> 考虑到使用CSV数据，不是用Excel，当在应用CSV数据时，Excel仍然可以用作数据编辑器，所以没有必要再在你的运行环境中安装CSV编辑器了。  


## CSV数据连接器  
>使用存储在CSV文件格式中的测试数据是一种选择。本节展示如何将这些测试数据添加和分配到数据驱动测试用例或智能文件夹。

![B1030-0000120](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000120.png)  

1. 单击数据源管理器中的`New`按钮，并单击`CSV`连接器…

2. 配置完成后，确认OK  


### CSV数据连接器配置

1. 为连接器指定一个有意义的名称，并使用标准的Windows对话框选择文件位置

2. 如果应用版本控制，则必须检查此选项。否则，你可能无法访问测试数据。即使没有，也强烈建议将测试文件复制到你的测试环境中。

3. 数据配置
   
    - 指定CSV文件是否包含头文件
    - 在启动时不加载CSV文件意味着没有确定行数，因此不能在测试套件中显示

4. 屏蔽数据项的选项将在本节末尾介绍和解释

## SQL数据连接器

SQL数据连接器允许你访问SQL数据库并通过使用SQL查询访问数据。在这里，一个访问Microsoft Access数据库的简单的基本示例演示了访问SQL数据库的基本原理

![B1030-0000130](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000130.png)  
*创建SQL数据连接器-部分1*

1. 单击数据源管理器中的`New`按钮，并单击SQL connector…
2. 为连接器分配一个有意义的名称
3. 单击`Create`继续指定SQL连接字符串

    ![B1030-0000140](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000140.png)  
    *创建SQL数据连接器-部分2*  
4. 在标准的Windows文件对话框中指定数据库位置
5. 完成可选连接属性后，单击`OK`继续  

    ### 可选的连接配置

        - 如果需要，在可选对话框中更改数据库连接类型
        - 如果需要，用用户名和密码指定登录数据
        - 建议在测试集成之前测试连接  

    ![B1030-0000150](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000150.png)  
    *创建SQL数据连接器-部分3*

6. 继续创建指定数据库查询

![B1030-0000160](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000160.png)  
*SQL数据库查询设计*  

完成必要的SQL查询，向Ranorex Studio提供必要的数据，并与OK进行确认

![B1030-0000170](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000170.png)
*创建SQL数据连接器-部分4*

7. 如果要结束，单机OK来结束SQL数据连接器的建立

## 数据屏蔽选项

数据连接器指定属性时，此选项允许在报告中隐藏特定数据。如果你需要将敏感的或涉密的测试数据在报告中“隐藏”，这个选项允许你指定在报告中隐藏数据。

![B1030-0000180](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000180.png)  
*报告中屏蔽数据*  

1. 没有被屏蔽的数据在报告中正常显示
2. 屏蔽的数据在报告中以点代替

## 选择数据范围

可以指定和选择一个数据范围，即基于完整行，为当前测试用例提供数据源的子集。

![B1030-0000190](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1030-0000190.png)  
*选择数据范围*

1. 在“数据属性选择”对话框中选择一个范围

2. 单击Preview effective data set查看选择的结果

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/data-driven-testing/data-data-management/
