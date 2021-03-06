# [译] 报告基本的特征和数据

*原文地址 👉 [Basic report characteristics & data][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-21*    

---

除了Ranorex报告的使用和应用外，还有在所有类型的报告中共享的报告特征和报告数据，本章的目的是介绍和解释它们。

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [基本特征](#基本特征)
- [报告中的动作](#报告中的动作)
- [报告中的测试验证](#报告中的测试验证)
- [记录分隔符](#记录分隔符)
- [用户定义的日志信息](#用户定义的日志信息)

## 基本特征

- 一旦测试运行开始，报告就开始收集数据
- 👉报告级别控制报告中包含的数据类型和数量
- 报告将在测试运行过程中生成，你可以在运行期间随时查看。这对于需要数小时运行的超大型测试套件特别有用

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 报告 \> 👉 [Ranorex标准报告][1]和[报告级别][2]探讨了这些基本特征

## 报告中的动作

基本上，在测试运行期间执行的每个操作都会默认触发状态消息，因此可以包含在测试报告中。

![A9020-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9020-0000010.png)  
*动作执行的报告示例*

**要点须知** 
- 每个执行的动作是报告中一个报告项
- 测试用例和测试运行通常很大，可能包含数千个要执行的动作。因此，报告中所有行动执行的表示将导致庞大且无法管理的报告
- 错误级别的概念有助于控制哪些测试运行事件进入报告
- 此外，动作的报告访问权限可以通过其动作属性来控制

### **控制动作的报告访问权限**

1. 在操作列表中选择一个操作
2. 按`F4`打开动作属性面板
3. 打开`Use logging`属性的下拉列表

![A9020-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9020-0000020.png)  
*控制动作的报告访问权限*  

1. `Default` -- 日志的默认设置可能是“true”或“false”。这是Ranorex Studio设置中指定的。

> **章节预览**  
> 在 \> Ranorex Studio 系统详情 \> 设置和配置 \> 👉 [报告设置][3]介绍和解释了设置和配置报告的完整选项

2. `True` -- 动作项被记录
3. `False` -- 动作项不被记录

## 报告中的测试验证

测试验证是一种特殊类型的操作

![A9020-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9020-0000040.png)  
*报告中成功和失败的验证*  

1. 成功的测试验证

    成功执行的测试验证操作将其状态消息与报告级别`Success`附加在一起，通常以绿色打印。

2. 失败的测试验证

    失败的验证操作通常会导致测试运行流产，并将其状态消息与报告级别`失败`附加在一起，并以红色打印。

**提示**  
> 测试验证失败后测试运行的默认中止可能没有用。因此，可以启用“失败继续执行”即`enabled to continue on fail’`


> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 动作 \> 👉 [管理动作][4]介绍和解释了失败后继续执行动作和动作管理的相关概念


### **控制测试验证的报告访问权限**

可以通过验证操作的属性窗格，控制报表对测试验证访问权限。

1. 选择测试验证动作
2. 按`F4`打开动作属性面板
3. 指定测试验证失败和成功的报告级别

![A9020-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9020-0000050.png)  
*报告对测试验证成功与失败的访问权限*  

## 录制分隔符

录制分隔符允许构建录制模块并提供一种通过报告消息使测试运行更加透明的简便方法。

> **章节预览**  
> 分隔符也是管理录音的各种选项的一部分，在 \> Ranorex Studio 基础教程 \> Ranorex 录制器 \> 👉 [管理录制模块][5]介绍和解释了相关概念

![A4060-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A4060-0000050.png)  
*插入分隔符操作*  

1. 点击`Separator`添加分隔符
2. 看到动作列表中的分隔符操作

### **结果**

因此，录制不仅是视觉结构。分隔符在报告中表示为报告行消息，其中包含分隔符头文本作为报告信息。

![A4060-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A4060-0000060.png)  
*报告中分隔符信息*  

**提示**  
> 分隔符拥有报告级别“Info”，这是下一章介绍的概念。

## 用户定义的日志信息

用户定义的日志消息是一种在需要时插入附加报告消息的方法。该方法主要用作调试工具，目的是在测试运行期间在特定位置生成报告消息。

1. 在动作列表中选择一个位置，然后打开 > `Add new action`下拉菜单
2. 单击 > `Log message` 以获取用户定义的日志消息

![A9020-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9020-0000060.png)  
*插入一条用户定义信息*  

### **结果**

1. 动作类型--“报告”

    日志消息的动作类型为“报告”，也可通过第1列中的操作图标显示

2. 报告类型

    可以通过打开相应的列表来指定报告类型

![A9020-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9020-0000070.png)  

- 日志: 日志操作的内容(即文本)或定义变量的内容显示在报告中
- 截图: 在执行时获取链接的控件库项的屏幕快照并存储在报表中
- 快照: 此选项触发Ranorex Spy，在执行时分析并存储相应链接控件库项的控件库状态并存储它。报告中的链接打开Ranorex Spy并显示控件库状态

3. 日志信息规范
   
- 第2列保存日志消息内容
- 这可以是常量值（即文本消息），也可以是对可以应用基于数据的测试的变量的引用

4. 错误级别

- 第5列概述了相应的错误级别

### **在报告中用户定义日志信息**

![A9020-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9020-0000090.png)  
*在报告中用户定义日志信息*  

1. 动作表中的用户定义日志消息
2. 在报告中生成的日志消息



[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/reporting/basic-report-characteristics-data/
[1]: .\[译]Ranorex标准报告.html
[2]: .\[译]报告等级概念.html
[3]: ..\\..\\..\\ranorex-studio-system-details/settings-configuration/[译]报告设置.html
[4]: ..\\..\\actions/[译]管理动作.html
[5]: ..\\..\\ranorex-recorder/[译]管理录制模块.html




