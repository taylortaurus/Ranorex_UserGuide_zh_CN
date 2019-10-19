# [译] 数据绑定

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月14日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月29日-green.svg?longCache=true&style=flat-square)

---
既然我们已经定义了变量并将数据源分配给测试用例，我们就可以连接它们了。这称为数据绑定，  这是本章的主题。


**本章导视**

- [初始情况](#初始情况)
- [访问数据绑定](#访问数据绑定)
- [将数据绑定到变量](#将数据绑定到变量)
- [自动绑定](#自动绑定)


**视频向导**
>视频“数据绑定”将引导您了解本章中的信息。              
[立即观看](https://www.youtube.com/embed/ustjQ5-mbr4)

## 初始情况
下图显示了初始情况，数据源已分配给测试用例，并且已定义但未绑定的变量位于记录模块旁边。

![B1040-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1040-0000010.png)


1. 数据源myCSVData带有分配给测试用例的8个数据行。

2. 5个记录模块中的6个未绑定变量。

## 访问数据绑定
1. 使用以下选项之一：

a. 右键单击测试容器，然后单击“数据绑定”。

b. 双击一个未绑定的变量。

![B1040-0000020](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1040-0000020.png)


### **数据绑定对话框**
数据绑定对话框打开，其中包含以下各项：

![B1040-0000030](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1040-0000030.png)

1. 测试容器的属性窗口中的“ 数据绑定”选项卡

2. 分配的数据源中可用数据列的列表

3. 多个包含定义的变量的下拉菜单可用于绑定

4. 自动绑定 功能， 在本章末尾说明

5. 取消绑定所有变量的数据列

## 将数据绑定到变量
将数据绑定到变量意味着每列指定一个变量。

对于FirstName列：

1. 打开数据列旁边的变量下拉列表。

2. 检查数据将绑定到的变量。在这种情况下：InsertName.txtFirstName


**注意**
>数据绑定对话框中的变量名称是定义它们的模块和它们的实际名称（不带$）的组合。因此，对于InsertName.txtFirstName，InsertName是记录模块，然后有一个分隔期，而txtFirstName是实际的变量名称。

![https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1040-0000040.png](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1040-0000040.png)


对于LastName列：

1. 打开数据列旁边的变量下拉列表。

2. 检查用于数据绑定的变量。在这种情况下：InsertName.txtLastName


**注意**
>仅显示未绑定的变量。缺少InsertName.txtFirstName，因为我们已经将FirstName列绑定到了它。

![B1040-0000050](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1040-0000050.png)

对其余的列/变量重复这些步骤。

### **结果**

![B1040-0000060](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1040-0000060.png)


1. 分配的数据源中可用数据列的列表。

2. 绑定变量列表。

### **结果测试套件视图**

![B1040-0000070](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1040-0000070.png)

1. 数据源myCSVData带有分配给测试用例的8个数据行。

2. 5个记录模块中的6个绑定变量。

我们的数据驱动测试现已完成。在下一章中，我们将运行它并获取报告。

## 自动绑定
此选项自动将数据源的所有数据列（即列标题）绑定到名称完全相同的变量。如果在设计数据源和命名变量时牢记这一点，则可以加快数据绑定过程。

![B1040-0000080](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1040-0000080.png)

---

[👈管理和分配数据源][1]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[执行数据驱动的测试👉][2]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/data-driven-testing/data-binding/

[1]:.\data-data-management.html
[2]:.\executing-data-driven-tests.html