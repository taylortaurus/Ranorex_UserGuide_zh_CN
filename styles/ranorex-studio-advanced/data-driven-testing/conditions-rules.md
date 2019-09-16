# [译] 条件和规则

*原文地址 👉 [Conditions & rules][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-14*    

---

条件和规则允许在Ranorex中对智能文件夹和测试用例进行更指定的控制和条件执行。本节将展示如何设置条件、定义规则，从而基于特定的参数控制执行。

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [定义测试示例](#定义测试示例)
- [添加条件](#添加条件)
- [添加并制定规则](#添加并制定规则)
- [条件设置](#条件设置)
- [条件类型](#条件类型)
- [完整的解决方案示例](#完整的解决方案示例)

## 定义测试示例

利用当前的测试示例，解释条件的定义和配置。假设，我们只想在测试数据库中插入`女性`数据

![B1060-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1060-0000010.png)  
*定义条件和规则的测试示例* 

**测试的定义:**
- 在常规测试中，8人被插入到演示应用程序数据库中
- 测试用例将以一种方式进行修改，即`只有女性被插入`到数据库中
- 此设置将由条件执行


## 添加条件

条件和规则可以应用于智能文件夹或测试用例。这个概念保持不变，并且很容易理解。

![B1060-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1060-0000020.png)  
*定义条件-部分1*  

1. 选择要设置条件的智能文件夹或测试用例
2. 打开上下文菜单并单击`Condition`

    ![B1060-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1060-0000030.png)  
    *定义条件-部分2*  

3. 单击`Add rule`开始定义当前条件的规则

**要点须知** 
1. 请参阅测试容器属性对话框窗口的条件选项卡
2. 为当前条件定义的所有规则的列表

**提示** 
一个条件可以被定义给一个智能文件夹或是测试用例


## 添加并制定规则

条件是基于规则的。最多有10条规则可以组合成一个条件。

![B1060-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1060-0000040.png)
*给条件指定一个规则*  

1. 数据源:数据类型的选择——可用的数据源是从文件中读取的数据源或从运行时设置的参数中获取的数据
2. 数据选择:根据之前的选择，列出可用的数据源/参数
3. 数据项:在任何可用的数据项中进行选择的选项(=列)
4. 条件运算符:条件运算符的选择
5. 关系引用选择:基于所选测试数据的条件引用选择

### 结果

![B1060-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1060-0000050.png)  
*测试套件视图中的状态指示器*

1. 测试套件视图中的条件测试用例或智能文件夹
2. 指示符显示测试用例或智能文件夹具有已定义的条件  

**贴士**  
> 条件可以包含最高10条规则

## 条件设置

本节概述了用于指定和设置条件的各种选项。

![B1060-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1060-0000060.png)  
*条件设置*  

1. 条件激活/失活:条件可以通过简单的点击复选框激活/失活
2. 条件设置:选择设置是否所有或任何规则驱动测试结果
3. 不完整规则定义指示符:如果规则不完整，则警告标志指示规则不完整的位置
4. 规则完整性指示器:一个小的指示器显示规则是完整的还是不完整的

## 条件类型

根据它们的完整性和激活状态，区分了三种情况:

![B1060-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1060-0000070.png)  
*条件类型*  

1. 具有一个或多个完整规则的活动状态
2. 具有一个或多个不完整规则的活动状态
3. 有一个或多个规则的不活动状态


## 完整的解决方案示例

下面是准备好的完整示例解决方案的链接。

**练习，我能做什么？** 
> 主题：数据驱动测试（完整示例解决方案）  
> 时间：30min以内  
> 下载：[点我下载][1]  

### 安装

1. 解压项目目录到你的计算机任一文件夹
2. 使用RanorexStudi打开`RxDatabase.rxsln`解决方案

**提示**  
> 示例解决方案适用于Ranorex版本8.0或更高版本。你需要将解决方案自动升级同意到8.2及更高版本的  


### 测试运行的准备工作

要使用准备或开发的示例解决方案运行条件，建议禁用测试验证记录模块`ValidateEntries`和`ExitAUT`记录模块。`ValidateEntries`会在当前设置中生成错误的验证结果，`ExitAUT`会阻止你看到条件结果，因为在测试运行后立即关闭演示应用程序。  

![B1060-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Data-drivenTesting/B1060-0000080.png)  
*条件化后的测试运行设置*






[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/data-driven-testing/conditions-rules/
[1]: https://www.ranorex.com/rx-media/rx-user-guide/v8.2/download/RxSampleDataDrivenTestingComplete.zip