# [译] 管理和分配数据源


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月4日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月29日-green.svg?longCache=true&style=flat-square)


---

**本章导视**

- [创建数据源](#创建数据源)
- [管理数据源](#管理数据源)
- [分配数据源](#分配数据源)
- [数据源类型和连接器](#数据源类型和连接器)
- [遮罩数据](#遮罩数据)
- [极限数据范围](#极限数据范围)
- [本章步骤摘要](#本章步骤摘要)

## 创建数据源
创建数据源与创建表一样容易。数据源的外观如何取决于您的测试，因此就如何设计数据源提出建议超出了本用户指南的范围。

要遵循我们的示例解决方案，您需要一个数据源。

[下载CSV表](https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxTestDatabase.zip)并将其解压缩到计算机上的任何目录，或者简单地将以下文本复制并粘贴到文本文件中，然后另存为.csv。


|名|姓氏|年龄|性别|部门|Num|
|:--|:--|:--|:--|:--|:--|
|John|公共|48|男性|项目管理|1|
|玛丽|史密斯|36|女|销售|2|
|亨利|罗杰斯|29|男性|支持|3|
|托马斯|巴赫|42 |男性|发展|4|
|Cindy|Martens|19|女|办公室|5|
|Hanna|Perry|48|女|管理|6|
|Will|Hallmark|32|男|支持|7|
|妮可|华莱士|38|女|测试|8|


## 管理数据源

数据源及其测试数据 包含，按测试套件进行管理。这意味着：

- 将数据源添加到测试套件后，可以将其分配给该测试套件的测试容器。
- 您无法从测试套件B访问测试套件A中的数据源。首先需要将数据源添加到测试套件B。
- 如果将数据源添加到每个测试套件中，则可以同时在多个测试套件中使用它。

要直接访问数据源管理：

a. 在测试套件视图中，单击“MANAGE DATA SOURCES... ”。

您也可以通过“Data source…”对话框访问数据源管理。选择测试容器后：

b. 单击测试套件工具栏中的“Data source”，然后单击“Manage data source...”。

c. 单击测试套件的上下文菜单中的“Data source...”，然后单击“Manage data source”。

![B1030-0000020](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000020.png)

### **数据源管理对话框**
出现数据源管理对话框，如下所示。要为我们的示例项目添加CSV数据源：

1. 点击New> CSV connector... 

![B1030-0000030](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000030.png)

1. 添加一个新的数据源。有四种不同类型，如下所述。
2. 删除现有的数据源。


**注意**
>删除简单的数据表意味着物理删除数据。数据将丢失！这是因为简单数据表直接存储在相应的测试套件文件中。
>
>在此对话框中删除Excel，CSV或SQL数据源意味着仅删除该数据源的连接器和“配置”部分中的设置，而不是数据源文件本身。

3. 克隆数据源。

对于简单的数据源，这意味着克隆数据源的内容和“配置”部分中的设置。对于所有其他数据源，这意味着克隆连接器和“配置”部分中的设置。例如，此选项对于指定同一Excel数据源的不同工作表很有用。
4. 已添加数据源的列表，每个数据源显示连接器类型（简单，CSV，Excel，SQL）和使用计数（测试套件中已分配数据源的次数）。

5. 配置部分。您可以在此处根据数据源类型管理某些设置。下面说明每种数据源类型的可用设置。

## 分配数据源

添加数据源后，需要将其分配给测试容器，以便其中的模块/变量可以访问数据。

为此：

1. 选择要分配数据源的测试容器。

2. 打开上下文菜单，然后单击Data source…。

![B1030-0000040](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000040.png)

3. 从下拉菜单中选择所需的数据源，然后单击“确定”。

4. 数据源显示在“测试套件”视图中的测试容器旁边，并指示其中的行数。

![B1030-0000050](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000050.png)

### **数据源分配规则**
将数据源分配给测试容器要遵循以下三个规则：

|规则1	|一旦分配给测试容器，就不能将数据源分配给该测试容器的后代。|
|:--|:--|
|规则二	|分配给测试容器后，该测试容器的所有后代都可以访问数据源的内容，但其兄弟姐妹或祖先不能访问该数据源。|
|规则三	|树中分配的多个数据源相互补充；他们不会互相取代。|


### **例子1**
让我们以示例的方式查看这些规则的工作方式。假设我们在测试套件中有两个数据源：CSV数据源myCSVData和Excel数据源，myExcelData。

![B1030-0000060](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000060.png)

1. CSV数据源已分配给智能文件夹A-1。

2. Excel数据源已分配给智能文件夹A-2。

3. 由于规则2，测试用例A及其模块无法访问后代测试容器的数据源。

4. 由于有规则2，智能文件夹A-1的模块可以访问CSV数据源。

5. 由于规则2和3，智能文件夹A-2的所有模块都可以访问CSV和Excel数据源。

6. 由于规则2和3，智能文件夹A-2的后代中的所有模块都可以访问CSV和Excel数据源。


### **例子2**

![B1030-0000070](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000070.png)

1. 在测试用例B和智能文件夹1下分配了所有数据源。因此，这些测试容器及其模块无法访问数据源。

2. Excel数据源已分配给智能文件夹1-1。因此，此树分支的后代（模块，测试容器）可以访问Excel数据源。

3. CSV数据源已分配给智能文件夹1-2。因此，其模块可以访问此数据源。

4. Excel数据源已分配给智能文件夹1-2-1。因此，它的后代可以访问CSV和Excel数据源。

5. Excel数据源也已分配给智能文件夹1-3-1。因此，它的后代可以访问此数据源。

## 数据源类型和连接器
Ranorex Studio支持四种不同类型的数据源：简单，CSV，Excel和SQL数据表。

除简单数据表外，所有这些源均通过连接器添加。这意味着Ranorex Studio仅链接到数据表文件。它不会将文件的内容添加到测试套件中。

### **简单数据表**

当您想快速设置小型数据驱动的测试（例如试验和错误）时，简单数据表非常有用。我们不建议它们用于比几个数据行更复杂的事情。

简单数据表及其所有内容都直接存储在测试套件文件（.rxtst）中。这就是为什么您必须直接在“ 数据源...”对话框中创建和维护它们的原因。这也是为什么在数据源管理对话框中将它们删除时将它们完全删除的原因，这与其他数据源不同。

要添加新的简单数据表：

1. 单击 New> Simple data source。

2. 命名数据源。

3. 单击确定。

![B1030-0000080](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000080.png)


1.该面具选项下面进一步分开说明。

4. 在测试容器的“ 数据源...”对话框中，选择简单数据源，然后在表编辑器中创建内容。

**贴士**
>您可以将表格从Excel文件粘贴到表格编辑器中。

![B1030-0000090](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000090.png)

5. 完成后，单击“确定”。

![B1030-0000100](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000100.png)


2.您还可以指定数据范围。该选项将在下面单独说明。


### **Excel数据连接器**

Excel数据源通过连接器添加。


**贴士**
>代替默认的Excel文件 格式 xlsx，您还可以使用本机二进制文件格式 xlsb。 Microsoft Office 2007和更高版本支持此文件格式，并且比非二进制版本要快得多。

要添加Excel连接器：

1. 单击 新建> Excel连接器…

2. 配置连接器，然后单击确定。

![B1030-0000110](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000110.png)


Excel连接器配置：

1. 命名 Excel连接器并指定 Excel文件的位置。

2. 这会将Excel文件复制到您的项目文件夹中。如果使用版本控制，则必须检查。


**贴士**
>强烈建议您在任何情况下都选中此选项。这样，您就不必担心测试数据文件的位置。此外，当您通过Ranorex Remote等部署测试时，文件将自动在运行时环境中传输到Ranorex代理。

3. 工作表选择

如果您的Excel文件包含多个工作表，则可以在此处指定要使用的工作表。您也可以将测试数据限制在特定范围内。

取消选中自动加载选项，以减少测试套件的启动加载时间。但是，这也意味着行数不会在测试容器旁边显示。

**贴士**

>使用“克隆”选项可以快速创建多个Excel连接器，这些连接器链接到同一文件，但工作表或范围不同。

4. 该面具选项下面进一步分开说明。

### **CSV数据连接器**

CSV数据源通过连接器添加。添加后，可以在Ranorex Studio的“ Data source…”对话框中编辑CSV数据源。通过单击“OK”或“Apply”保存这些更改时，实际的CSV文件也将更改。

要添加CSV连接器：

1. 单击新建> CSV连接器...

2. 配置连接器，然后单击确定。

![B1030-0000120](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000120.png)

CSV连接器配置：
1. 命名 CSV连接器并指定 CSV文件的位置。

2. 这会将Excel文件复制到您的项目文件夹中。如果使用版本控制，则必须检查。

3. 资料配置

指定CSV文件是否包含标题行。取消选中自动加载选项，以减少测试套件的启动加载时间。但是，这也意味着行数不会在测试容器旁边显示。

4. 掩膜选项将在下面单独解释。


### **SQL数据连接器**

使用SQL数据连接器，您可以访问SQL数据库并使用SQL查询从数据库中提取数据。我们将通过一个访问Microsoft Access数据库的简单示例来说明此过程。

1. 单击新建> SQL连接器…
2. 为连接器命名。
3. 单击创建以指定SQL连接字符串。

![B1030-0000130](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000130.png)

4. 指定数据库文件的位置。

5. 指定可选的连接设置（请参阅下文），然后单击“确定”。


### **可选的连接设置：**
a.更改数据库连接类型以适合您的数据库类型。在我们的示例中，Microsoft Access数据库文件是正确的，因为我们使用的是Microsoft Access数据库。

b.如果数据库需要登录，请在此处指定。

c.单击以测试到数据库的连接（推荐）。

![B1030-0000140](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000140.png)


6. 在查询下，单击创建以指定数据库查询。

![B1030-0000150](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000150.png)


7. 在数据库（在我们的示例中为Microsoft Access）中定义所需的SQL查询，以将数据提供给Ranorex Studio，然后单击“确定”。

![B1030-0000160](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000160.png)

8. 设置自动加载行为（为加快加载速度而禁用，但在测试套件视图中缺少行指示符）和屏蔽（在下面单独说明），然后单击确定。

![B1030-0000170](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000170.png)

## 遮罩数据
您可以屏蔽所有数据源类型的数据。这样，您可以在报表中隐藏敏感数据，同时仍允许Ranorex Studio对其进行访问以进行测试。

![B1030-0000180](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000180.png)

1. 未屏蔽 列中的数据将正常显示在报告中。
2. 蒙版列中的数据隐藏在报告中。


## 极限数据范围
您可以限制所有数据源的数据范围。这使您只能使数据源的某些行可用于测试容器。

1. 在“ 数据源…”对话框中输入行范围。

2. 点击预览有效数据集…以查看结果。

![B1030-0000190](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1030-0000190.png)

## 本章步骤摘要
现在，我们已经解释了用于管理和分配数据源的所有选项，让我们快速完成所有必要的步骤，为下一章再次准备示例解决方案。

1. 确保您已准备好数据源（CSV文件）。

2. 在测试套件视图中，单击“管理数据源...”。

3. 点击新建> CSV连接器...

4. 将其命名为myCSVData，指定文件的位置，选中所有三个框，然后单击OK。

5. 在测试套件视图中，右键单击测试用例Data-driven_DB_Test，然后单击数据源…。

6. 在下拉菜单中，选择myCSVData，然后点击确定。

现在，您已经分配了数据源。您的解决方案已准备好进行下一步：数据绑定。

---

[👈定义变量][1]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[数据绑定👉][2]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/data-driven-testing/data-data-management/

[1]: .\preparations-data-driven-testing.html
[2]: .\data-binding.html