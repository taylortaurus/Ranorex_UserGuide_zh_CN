# [译] 条件和规则

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月14日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月29日-green.svg?longCache=true&style=flat-square)
 

---

条件和规则使您可以进一步控制测试执行。顾名思义，他们根据是否满足特定条件执行测试。有条件的执行取决于来自数据源或参数的值，这就是为什么将本主题解释为数据驱动测试的一部分的原因。

在本章中，我们将向您展示如何使用简单的规则来设置条件以创建条件测试用例。我们将逐步解释相关设置。您可以在本章末下载完整的示例。

**本章导视**

- [下载样本解决方案](#下载样本解决方案)
- [测试场景](#测试场景)
- [添加条件](#添加条件)
- [定义规则](#定义规则)
- [条件设定](#条件设定)
- [条件状态](#条件状态)
- [运行测试](#运行测试)
- [下载完整的样本解决方案](#下载完整的样本解决方案)









**视频向导**
>视频“条件”将引导您了解本章中的信息。             
[立即观看](https://www.youtube.com/embed/rRooHNJ5-X8)

## 下载示例解决方案
要遵循本章中的说明，请从下面的链接下载示例解决方案文件。


**注意**
>我们已在此解决方案中禁用了两个模块，因为它们会干扰条件（验证）或阻止您在Ranorex Studio演示应用程序中查看结果（拆卸）。

**示例解决方案**
>主题：条件          
时间：15分钟                
[立即下载](https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleDataDrivenConditionStart.zip)


安装示例解决方案：
1. 解压缩到计算机上的任何文件夹。

2. 启动 Ranorex Studio并打开解决方案文件RxDatabase.rxsln


**贴士**
>示例解决方案可用于Ranorex 8.0或更高版本。您必须同意8.2及更高版本的自动解决方案升级。

## 测试场景
对于我们的示例，我们将使用前几章的数据驱动测试。仅这次，我们只想将女性员工插入Ranorex Studio演示应用程序的数据库中。

![B1060-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1060-0000010.png)


综上所述：
- 通常，将8名工作人员插入数据库。
- 我们想要修改测试用例，以使其仅将女性职员输入数据库。
- 我们要有条件地做到这一点。


## 添加条件
- 您只能将条件添加到测试用例或智能文件夹。
- 每个测试容器只有一个条件。
- 条件可以包含一个规则或由多个规则定义。
- 两种类型的测试容器的整个过程都是相同的。

要添加条件：

1. 右键单击要添加条件的智能文件夹或测试用例。

2. 点击条件...

![B1060-0000020](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1060-0000020.png)


3. 单击添加规则以为此条件定义一个规则。

![B1060-0000030](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1060-0000030.png)

1. 测试容器属性对话框的“ 条件”选项卡。

2. 非活动状态，尚未在其下定义任何规则。

## 定义规则
条件由规则定义。您最多可以为一个条件添加10条规则。规则始终遵循相同的模式，并检查数据源或参数值是否等于控制值。

1. 通过选择所需的详细信息从左到右定义一个规则，完成后单击“确定”。

![B1060-0000040](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1060-0000040.png)

1. 数据源/参数：选择要检查的值是在数据源中还是在参数中。

2. 特定数据源/参数：选择特定数据源，还是选择包含值的本地/全局参数。

3. 列/行：选择包含该值的列（数据源）或行（参数）。

4. 操作员：选择要检查的值必须等于或不等于控制值。

5. 控制值：从数据源/参数中选择一个可能的控制值。

**结果**
如果您如上所述定义规则，那么您现在将获得一个条件，其中包含一个完整的规则。在测试套件视图中，这将指示如下：

![B1060-0000050](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1060-0000050.png)

1. 有条件的测试用例。

2. 指示测试用例具有活动的已定义条件的指示器。

## 条件设定
除了我们已经使用的条件对话框外，条件对话框还具有各种设置：

![B1060-0000060](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1060-0000060.png)              
*条件设定*

1. 激活复选框：在活动/不活动状态之间快速切换。不删除任何定义的规则。

2. 条件运算符：设置何时满足条件并运行测试容器。

3. 规则不完整指示器：出现在规则缺少信息的任何地方。

4. 规则完整性指示器：显示规则是完整还是不完整。

## 条件状态
根据其完整性和激活状态，条件在测试套件视图中由三个不同的符号指示：

![B1060-0000070](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1060-0000070.png)


1. 具有一个或多个完整规则的活动状态。

2. 具有一个或多个不完整规则的活动状态。

3. 具有一个或多个完整或不完整规则的非活动状态。

## 运行测试
我们已经完成了条件并准备运行测试。照常从测试套件视图运行测试。您会注意到Ranorex Studio演示应用程序中的数据库仅包含女性员工。该报告还将反映条件，并在未满足条件的迭代中将其标记为“已阻止”：

![B1060-0000090](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1060-0000090.png)


## 下载完整的样本解决方案
您可以下载完整的示例解决方案，并执行本章中的所有步骤并准备运行：

**示例解决方案**
>主题：条件             
时间：15分钟         
[立即下载](https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleDataDrivenConditionDone.zip)


### **安装示例解决方案：**
1. 解压缩到计算机上的任何文件夹。

2. 启动 Ranorex Studio并打开解决方案文件RxDatabase.rxsln

**贴士**
>示例解决方案可用于Ranorex 8.0或更高版本。您必须同意8.2及更高版本的自动解决方案升级。

---

[👈参数][1]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/data-driven-testing/conditions-rules/
[1]: .\parameters.html