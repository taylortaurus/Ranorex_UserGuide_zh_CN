# [译] 复杂的报告定制

*原文地址 👉 [User-defined reporting][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-25*    
*♋ update time : 2019-9-10*

---

在本章中，您将找到有关如何执行一系列更复杂的报表自定义的说明。由于它们需要编码技能，因此您应该熟悉Ranorex Studio中的代码模块。

>**章节预览**              
如果您不熟悉代码模块及其应用程序的概念，请参阅Ranorex Studio专家>  ⇢[代码模块][4]。




**本章导视**

- [示例解决方案](#示例解决方案)
- [应用Ranorex标准报告类](#应用Ranorex标准报告类)
- [自定义报告策略](#自定义报告策略)
- [用户定义报告级别](#用户定义报告级别)
- [设置当前报告级别](#设置当前报告级别)
- [覆盖当前报告级别](#覆盖当前报告级别)
- [报告截图](#报告截图)
- [报告系统摘要](#报告系统摘要)
- [添加自定义数据](#添加自定义数据)
- [应用自定义数据](#应用自定义数据)

## 示例解决方案

本文介绍了用户定义的报告方法的概念，下述提供示例解决方案下载。

**示例解决方案**            
> 主题：用户定义报告  
> 时间：30min以内  
> 下载：[点我下载][1]  

**安装**

1. 解压项目目录到你的计算机任一文件夹
2. 使用RanorexStudi打开`Introduction.rxsln`解决方案

**贴士**  
示例解决方案适用于Ranorex版本8.0或更高版本。你需要将解决方案自动升级同意到8.2及更高版本的。


## 应用Ranorex标准报告类
在代码中创建报告消息的最简单方法是使用六种不同的标准报告类之一。

### **标准报告类**
Ranorex Studio有六个标准报告类，如下所示。这些类对应于标准报告级别。

```java
Ranorex.Report.Debug(“Debug message”);
Ranorex.Report.Info(“Information message”);
Ranorex.Report.Warn(“Warning message”);
Ranorex.Report.Error(“Error message”);
Ranorex.Report.Success(“Success message”);
Ranorex.Report.Failure(“Failure message”);
```

1. 创建一个代码模块并打开它。
2. 在Run（）方法中添加标准报告类的类实例。

![A9060-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000010.png)
*应用Ranorex标准报告类*  


3. 从测试套件运行代码模块并查看结果

![A9060-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000020.png)  
*标准报告类的报告信息*  

**贴士**  
> 确保将测试套件的错误级别设置为“调试”级别，以显示所有标准报告消息。

### 用户代码操作的报告

当然，除了可以在代码模块中应用用户定义的报告之外，还可以通过用户代码操作将它们添加到录制模块中。

> **章节预览**  
> 如果您不熟悉用户代码操作及其应用程序的概念，我们建议您阅读 \> Ranorex Studio 基础教程 \> 动作 \> 👉 [用户代码动作][2]章节

1. 切换到录制模块`Recording1`(在示例解决方案中)  
2. 插入新的用户代码操作`ReportInformation()`，然后双击它以将其打开

![A9060-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000030.png)  
*在录制模块中插入用户代码动作*  

3. 将新报告信息消息添加到用户代码操作的构造函数中
4. 运行报告模块并在测试报告中查看报告消息

![A9060-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000040.png)  
*在用户代码中添加报告信息*  




## 自定义报告策略

用户定义的报告消息的默认类别是“用户”。 此默认类别可以随意更改。

### 临时定义的自定义报告类别

1. 创建一个新的代码模块`CustomReportCategory`，或从示例解决方案中打开它
2. 打开代码模块并添加以下介绍的代码

![A9060-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000050.png)  
*定义一个零时的自定义报告策略*  

1. 使用临时定义的自定义报告类别创建报告消息
2. 创建第二个报告消息，不定义自定义报告类别

### 结果

运行相应的代码模块并查看结果

![A9060-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000060.png)  
*零时设置自定义报告策略*  

3. 查看使用临时设置的自定义报告类别的报告消息

### 永久定义的自定义报告类别

1. 创建一个新的代码模块`CustomReportCategory`，或者从示例解决方案中打开它
2. 打开代码模块并添加下面介绍的代码

![A9060-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000070.png)  
*定义永久的自定义报告类别*  

1. 定义永久的默认自定义报告类别
2. 创建报告消息

### **结果**



![A9060-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000080.png)  
*永久设置自定义报告类别*

3. 查看使用永久设置的自定义报告类别的报告消息

## 用户定义报告级别

使用Ranorex，可以创建和应用具有名称和值的用户定义报表级别。在示例解决方案的代码模块`CustomReportLevel`中找到相应的示例。

1. 定义两个用户定义的报告级别`MID`和`LOW`
2. 将用户定义的报告级别应用于报告消息


![A9060-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000090.png)          
*用户定义的报告级别*  


![A9060-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000100.png)                
*具有用户定义的报告级别的测试报告*  

### **结果**
1. 查看测试报告中对应的报告信息
2. 相应地应用用户定义的报告级别

### **格式化用户定义的报告级别**

![A9060-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000110.png)  
*格式化用户定义的报告级别*  

5. 在CSS格式语法中定义样式格式
6. 查看测试报告中格式化的结果

## 设置当前报告级别

只有当报表级别高于或等于测试容器的报表级别时，报表信息才会出现在报表中。在示例解决方案的代码模块`CustomReportLevel`中找到相应的示例。

1. 定义两种用户定义的报告级别
2. 设置当前的报告级别值为`MID`和更高
3. 通过创建具有不同报告级别的两个报告消息来应用该设置


![A9060-0000120](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000120.png)  
*设置当前报告级别*  



### **结果**


![A9060-0000130](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000130.png)  
*测试报告包含经过级别筛选的报告消息*

1. 测试报告中仅包含报告级别为MID或更高级别的报告消息

## 覆盖当前报告级别

通过使用报告级别“始终”记录信息，可以始终覆盖当前报告级别。在示例解决方案的代码模块`CustomReportLevel`中找到相应的示例。

![A9060-0000140](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000140.png)                        
*覆盖当前报告级别*  


1. 定义两个用户定义的报表级别
2. 将当前报表级别设置为`MID`或更高
3. 通过创建两个报告消息来应用该设置，第二个消息覆盖当前报告级别

### 结果


![A9060-0000150](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000150.png)  
*覆盖当前报告级别*  

4. 看到第二个报告信息覆盖了当前的报告级别`MID` 


## 报告截图

添加以下代码以将屏幕截图发送到报告。如果您未指定存储库项目，Ranorex Studio会截取代码执行时可见的内容。

![A9060-0000160](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/A90/A9060-0000160.png)  
*报告的桌面截图*    

1. 添加用于将屏幕截图发送到测试报告的代码



> **章节预览**  
> 在 \> Ranorex Studio 专家教程 \> 👉 [代码模块][3]章节中介绍并解释了通过代码模块寻址控件库项目

## 报告系统摘要

添加以下代码以在报告中显示系统摘要。

![A9060-0000170](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/A90/A9060-0000170.png)  
*报告系统摘要*  

系统摘要在报告中显示为Info消息

## 添加自定义数据

在本节中，我们将向您展示如何在测试运行期间收集自定义数据以及如何将这些数据写入用于生成最终报告的XML测试数据文件中。

### 添加自定义数据到测试数据文件

触发定制数据收集是通过用户代码动作完成的，该动作具有待定义的方法并且负责跟踪定制数据。您可以在示例解决方案的代码模块`CustomData`中找到相应的示例。

![A9060-0000180](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000180.png)
*生成自定义报告数据*  

1. 活动堆栈对象定义
    - 定义一个引用Ranorex当前活动堆栈的对象
    - 活动堆栈是测试运行期间通过堆栈数据结构收集所有活动的地方
2. 将活动添加到“活动堆栈”
    - 活动堆栈方法`CustomProperties`将一个报告的活动放到活动堆栈上
    - 该方法由一个自定义字段名(即'myName')和一个自定义字段值(即'myValue')定义，它们都是string类型的 

### 结果

运行代码模块并查看测试报告。

![A9060-0000190](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000190.png)  
*在测试数据文件中的自定义报告数据*

3. 测试数据文件中的自定义数据
    - 如果您在Ranorex报告生成之外应用测试数据，请随意以您需要的方式解析XML文件
    - 如果您需要将定制的测试数据包含在Ranorex标准报告中，请参阅下一节 

## 应用自定义数据

如果您希望将XML测试数据文件中的自定义数据包含在Ranorex报告中，请按照此处的说明进行操作。

> **章节预览**  
> 为了能够更改Ranorex标准报告的布局和内容，建议你对HTML，CSS，XSL和XML有基本的了解。 有关详细信息，请参阅[www.w3.org][2]上的万维网联盟（W3C）

### 自定义XSL文件

要在Ranorex报告中包含自定义数据，必须定制Ranorex报告的XSL规范。XSL规范的定制可以用任何XML编辑器完成，当然也可以用Ranorex Studio完成。您可以在示例解决方案的项目文件文件夹`/CustomDataTemplate/`中找到对应的XSL文件。

![A9060-0000200](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000200.png)  

4. 识别测试数据文件中的字段对
5. 打印定制数据介绍(头)选项
6. 选择对应字段名称的字段值

### 结果

![A9060-0000210](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9060-0000210.png)  
*在测试报告中的自定义数据*  

7. 根据XSL文件规范中的位置，Ranorex报告包含自定义数据

---

[👈定制化报告][5]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[将报告转换为其他数据类型👉][6]


[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/reporting/user-defined-reporting/
[1]: https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleUserDefinedReport.zip
[2]: ..\\..\\ranorex-studio-fundamentals/actions/[译]用户代码动作.html
[3]: ..\\..\\..\\ranorex-studio-expert/Code_modules/introduction.html
[4]: .\ranorex-studio-expert\code-modules\introduction.html
[5]: .\report-customization.html
[6]: .\converting-reports-data-types.html







