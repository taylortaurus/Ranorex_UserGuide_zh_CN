# [译] Ranorex标准报告

*原文地址 👉 [Ranorex standard reporting][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-25*    
*♋ update time : 2019-9-10* 

---

在本章中，您将了解报告的存储位置，报告内容，读取方式以及更改报告设置的位置。

**本章导视**

- [文件名和位置](#文件名和位置)
- [报告标题](#报告标题)
- [查看报告详情](#查看报告详情)
- [简单报告结构](#简单报告结构)
- [详细报告内容](#详细报告内容)
- [报告中的数据迭代](#报告中的数据迭代)
- [在测试报告中迭代运行](#在测试报告中迭代运行)
- [过滤信息](#过滤信息)
- [跳转](#跳转)
- [在Spy中打开](#在Spy中打开)
- [视频报道](#视频报道)
- [渐进式报告预览](#渐进式报告预览)
- [报告设置和配置](#报告设置和配置)

>**视频向导**              
视频“标准报道”将引导您完成本章中的信息。                
[立即观看](https://www.youtube.com/embed/NKZNwnugXYg)



## 文件名和位置

### **文件名**

报告名是自动生成，并根据测试是从录制模块还是从测试套件运行而更改。

![A9040-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9040-0000010.png)  

- 对于在测试套件开始的运行，文件名将以测试套件的名称开始
- 对于从录制模块开始的运行，文件名将以记录的名称开始
- 报告名称的第二部分是生成报告的日期和时间的组合
    - 测试日期 = 21 February 2018 = 2018221
    - 测试时间 = 07:08:36 PM = 190836
- 日期和时间用下划线分隔。
- 文件后缀是`.rxlog`，Ranorex Log的缩写

>**章节预览**  
> 你可以自定义生成报告文件名的方式，在 \> Ranorex Studio 系统详情 \> 设置和配置 \> 👉 [报告设置][2]章节中详细介绍和解释了相关内容

### 报告文件位置

在项目视图中，报告保存在你项目的`Reports`文件夹中。

![A9040-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9040-0000020.png)  
 
在Windows中，您可以从两个不同的文件夹访问报告。原始报告以及报告的布局文件和原始数据文件（稍后作为自定义的一部分进行说明）存储在输出目录的Reports文件夹中。

项目文件夹中的 “ 报告”文件夹仅包含原始报告的快捷方式，不包含任何样式表或原始数据文件。

请看这里的插图：

![A9040-0000031](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/A90/A9040-0000031.png)

1. 报告项目文件夹中的文件夹。

2. 报告项目输出目录中的文件夹。

3. 报告的布局文件。

4. 原始报告文件的快捷方式。

5. 包含原始数据文件的原始报告文件。


>**贴士**                 
对于您在Ranorex Studio 9中使用但在早期版本中创建的解决方案，动作略有不同：            
原始报告以及布局和原始数据文件直接存储在项目的输出目录中，而不是收集在Reports文件夹中。

### **报告标题**

报告标题显示一系列有用的数据并总结测试结果。

![A9040-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9040-0000050.png)  
基本的报告数据

1. 测试套件名/录制模块名
    - 运行测试的测试套件或录制模块的名称
2. 系统和测试数据
3. 错误和警告数量  
    - 如果报告中至少有一个警告，橙色通知将在下面进一步显示
4. 测试结果
    - 饼图总结了测试结果 

>**提示**  
> 此图表仅计算测试用例。智能文件夹被忽略;你可以在下面的报告详细信息中查看其结果。

![A9040-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9040-0000070.png)  
*报告汇总类型*  

5. 成功的测试
    - 绿色饼图表示所有测试用例都成功   
6. 失败的测试
    - 红色饼图表示所有测试用例都失败了 
7. 测试总结
    - 包含成功，失败和阻止测试用例的饼图
    - 在该示例中，运行配置包含8个测试用例。前两个测试用例成功通过。第三次失败，之后测试中止，阻止了剩下的5个测试用例
 
## 查看报告详情

默认情况下，测试用例、智能文件夹等的详细信息将被折叠。需单击项目名称旁边的箭头以显示详细信息。

![A9040-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9040-0000080.png)  


## 简单报告结构

报告的结构基本上遵循测试套件结构和执动作作的顺序。每个测试套件结构元素都存在于报表中，由于报表级别的设置，其内容可见/部分可见/不可见。

![A9040-0000120](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9040-0000120.png)  


1. 测试报告结构代表相应的测试套件结构
2. 报告信息表示相应录制模块的动作列表

## 详细报告内容

![A9040-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9040-0000090.png)  

1. 时间
    - 默认情况下，将显示从开始运行测试后的相对执行时间。在 👉 报告设置中，默认设置可以更改
2. 级别
    - 第二列显示所执动作作的报告级别
3. 类别
    - 此列显示已执行的动作类型
4. 消息
    - 报告消息包含有关执动作作期间发生的更多详细信息

![A9040-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9040-0000100.png)  
*报告消息，指出在特定控件库项目上执行了键序列'Harry'*  

如果发生故障，报告还将包括两个屏幕截图，一个在故障时刻，一个在故障发生之前。

![A9040-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9040-0000110.png)  

1. 失败的测试动作之前的动作截图
2. 测试测试动作的截图

## 报告中的数据迭代

在数据驱动的测试中，绑定了数据的测试用例或智能文件夹会根据数据源进行多次迭代。在报告中，每个迭代都单独显示。

![A9040-0000130](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9040-0000130.png)  
*报告中的数据迭代*  

1. 数据迭代
    - 数据迭代由＃行和数据行：测试容器旁边的＃标签表示
    - ＃行表示数据容器将被迭代的次数-每行一次
2. 测试报告中的数据行
    - 每个数据行/迭代及其详细信息都显示在报告中
3. 变量和值
    - 此迭代中使用的变量和值

>**提示**  
> - 可以在数据源对话框中屏蔽秘密测试数据。这也适用于报告。            
> - 例如，如果屏蔽了年龄和性别，报告将如下所示：

![A9040-0000140](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9040-0000140.png)  
*屏蔽的报告数据*  

> **章节预览**  
> 在 \> Ranorex Studio 高级教程 \> 👉 [数据驱动测试][1]章节中详细介绍和解释了`数据迭代和屏蔽数据`的概念  

## 在测试报告中迭代运行

如果迭代运行测试用例或智能文件夹，则每个运行迭代都会在报告中显示其详细信息

![A9040-0000150](https://www.ranorex.com/rx-media/rx-user-guide/latest/A90/A9040-0000141.png)  
*在测试报告中迭代运行*  

- 运行迭代由迭代指示：＃和运行：测试容器旁边的＃标签
- 迭代：＃告诉你测试容器的运行次数

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 测试套件 \> 👉 [运行测试][2]章节中详细介绍和解释了`数据迭代和屏蔽数据`的概念

## 过滤消息
报告中有两个过滤器：一个用于过滤测试容器，另一个用于过滤动作的消息。

### **过滤测试容器**

使用报表上部的复选框根据测试容器的成功状态对其进行筛选。

![A9040-0000160](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9040-0000160.png)  
*过滤报告消息*  

1. 成功--如果选中，则显示报告级别为“成功”的报告消息，前提是如果这些消息根据报告级别包含在报告中。如果未选中，则隐藏这些消息
2. 失败--选中时显示报告级别为“失败”的报告消息。如果未选中，则隐藏这些消息
3. 阻止--选中时显示测试运行的阻止测试用例。如果未选中，则隐藏阻止的测试用例

>**提示**  
> 被阻止的测试用例或智能文件夹是由于测试中止而未在测试运行期间执行的测试单元，或者未在测试套件中选择用于运行执行的测试单元。

### **过滤动作消息**
您还可以按报告级别过滤模块中的动作消息。

![A9040-0000161](https://www.ranorex.com/rx-media/rx-user-guide/latest/A90/A9040-0000161.png)



## 跳转

你可以直接从报告消息跳转到Ranorex Studio中的相应动作或测试套件项目

1. 鼠标移到报表条目上，即测试容器或动作的报表消息
2. 单击报表条目右上角的跳转到项按钮

![A9040-0000170](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9040-0000170.png)  

1. 跳转按钮
2. 与链接的控件库项相关联的动作

## 在Spy中打开

当你在Ranorex Studio外部打开报告时，`Open In Spy`按钮将可用。单击按钮以在Ranorex Spy中打开相应的报告项目

![A9040-0000172](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9040-0000172.png)  

1. 在报告中打开Spy的功能

## 视频报告
视频报告允许您将测试运行记录为视频集合。这也适用于Ranorex代理。

### **启用视频报告**
默认情况下禁用视频报告。您可以在👉报告设置中启用和配置它。

### **播放报告中的视频报告**
在报告中，单击测试用例旁边的播放视频以播放相应的视频。

![A9040-0000183](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/A90/A9040-0000183.png)

### **视频目录**
视频保存在Reports文件夹的输出目录中。对于每次测试运行，都会创建一个单独的文件夹。

![A9040-0000185](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/A90/A9040-0000185.png)

1. 报告输出目录中的文件夹

2. 三个视频文件夹



## 渐进式报告预览

Ranorex在测试运行过程中生成报告，你可以在测试运行期间的任何时候查看报告。这对于非常长的测试运行特别有用。

- Ranorex在测试运行一开始就开始生成报告
- 一旦设置的自动保存时间结束(默认= 30s)，就会保存报表文件
- 发生这种情况，只需双击报表文件就可以打开正在进行的报表

![A9040-0000191](https://www.ranorex.com/rx-media/rx-user-guide/latest/A90/A9040-0000191.png)  
*渐进式报告，带有两个通知，表明测试仍在进行中*

**提示** 
> 当然，如果你尝试在运行测试的计算机上打开报告，则很可能会导致测试失败，因为你将与UI进行交互。

## 报告设置和配置

报告有自己的设置。以下方式可以访问：

1. 在测试套件视图中，右键点击测试套件
2. 点击属性
3. 点击报告选项卡

![F3040-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/F3040-0000010.png)  
*报告设置*  


> **章节预览**  
> 在 \> Ranorex Studio 系统详情 \> 设置和配置 \> 👉 [报告设置][3]章节中详细介绍和解释了测试报告设置的相关内容

---

[👈报告等级][4]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[定制化报告👉][5]




[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/reporting/ranorex-standard-reporting/
[1]: ..\\..\\..\\ranorex-studio-advanced/Data-driven_testing/introduction.html
[2]: ..\\..\\test-suite/[译][译]执行测试套件.html
[3]: ..\\..\\..\\ranorex-studio-system-details/settings-configuration/[译]报告设置.html
[4]:concept-report-levels-2.html
[5]:.\report-customization.html