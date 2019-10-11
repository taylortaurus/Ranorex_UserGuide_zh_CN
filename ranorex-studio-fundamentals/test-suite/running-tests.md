# [译] 执行测试套件

*原文地址 👉 [Execute a test suite][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2019-9-6*  

---
在本章中，您将了解控制测试运行和在测试套件视图中执行测试的各种选项。

**本章导视**
- [下载示例解决方案](#下载示例解决方案)
- [管理运行配置](#管理运行配置)
- [禁用/启用测试套件项目](#禁用/启用测试套件项目)
- [配置运行迭代](#配置运行迭代)
- [配置自动重试](#配置自动重试)
- [配置报告级别](#配置报告级别)
- [配置错误行为](#配置错误行为)
- [从测试套件视图运行测试](#从测试套件视图运行测试)
- [Ranorex Test Suite Runner](#RanorexTestSuiteRunner)


>**视频向导**   
>视频“测试套件执行选项”将引导您完成本章中的信息。   
>[立即观看](https://www.youtube.com/embed/t7cxrUKnIic)

## 下载示例解决方案
本章中的解释基于示例解决方案。你可以在下面下载。

>**示例解决方案**   
>主题：测试套件运行   
>时间：不到10分钟   
>[下载示例文件](https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleTestSuiteRun.zip)

### **安装**：

1. 解压缩到计算机上的任何文件夹。

2. 启动 Ranorex Studio并打开解决方案文件RxDatabase.rxsln

>**贴士**   
>样本解决方案适用于Ranorex 8.0或更高版本。您必须同意8.2及更高版本的自动解决方案升级。


## 管理运行配置
您可以在测试运行中包含和排除测试用例和智能文件夹。为此，只需在测试套件中选中或取消选中它们即可。

![A5030-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5030-0000010.png)      
*要包含/排除的复选框 来执行测试*

已检查/未检查的测试用例和智能文件夹的当前状态称为运行配置。您可以保存运行配置以便重复使用，并使用测试套件视图中的下拉菜单在它们之间切换。

![5030-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5030-0000020.png)      
*管理运行配置*

1. 单击`运行配置`下拉菜单。
2. 单击`Manage run configurations...`

![5030-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5030-0000030.png)     
*添加新的运行配置*

3. 单击`Add`。
4. 给新的运行配置一个有意义的名字。
5. 单击`OK`。

### **结果**
可以从下拉菜单中选择运行配置。

![5030-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5030-0000040.png)      
*不同的运行配置*

1. TestRun配置包括所有测试套件元素
2. TestWithoutValidation配置不包括验证智能文件夹


## 禁用/启用测试套件项目
与包含/排除测试用例和智能文件夹类似，您还可以启用和禁用录制模块，代码模块，模块组和Setup和teardown地区。在测试运行期间不执行禁用的项目。

![5030-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5030-0000050.png)        
*禁用录制模块*

1. 右键单击要禁用的项目。
2. 单击禁用,该项目将显示为灰色。

>**贴士**
> - 禁用模块组会禁用此模块组中的所有模块。
> - 禁用Setup/teardown区域将禁用其中的所有项目。



## 配置运行迭代
默认情况下，测试用例和智能文件夹在测试执行期间运行一次。但是，您可能希望多次运行它们。您可以通过运行迭代来完成此操作。

![5030-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5030-0000060.png)     
*配置运行迭代*


1. 选择测试用例或智能文件夹后，按F4。
2. 该属性垫出现在测试套件的权利。
3. 在迭代计数旁边，设置所需的迭代次数。

迭代次数的属性。

### **结果：**
- 迭代次数显示在测试套件项旁边。
- 在我们的示例中，测试用例重复5次。

![5030-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5030-0000070.png)

## 配置自动重试
在UI测试中，有时会发生错误，因为测试中的应用程序没有响应。在这些情况下，一种解决方案是简单地重新运行部分测试。您可以使用自动重试执行此操作。具有自动重试计数的测试用例或智能文件夹将重新运行，直到它们成功 或 所有重试都已用完为止。

![5030-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5030-0000080.png)      
*配置自动重试*

1. 选择所需的测试用例或智能文件夹。 
2. 按F4。该属性垫出现在测试套件的权利。
3. 在`Retry count`旁边，设置所需的重试次数。

1.在属性中重试计数。

>### **贴士**
>如果存在数据绑定或运行迭代，则重试将从失败点开始。例如，如果失败发生在5的迭代3，那就是重试开始的地方   
>只有在每次重试失败的测试用例或智能文件夹才会在报告中标记为失败。

## 配置报告级别
您还可以在测试套件中设置测试用例和智能文件夹的报告级别。通过报告级别，您可以控制  报告中显示的信息及其显示位置。这对于包含许多测试用例和智能文件夹的复杂测试尤其有用，可以保持报表的结构化。

>**章节预览**   
>报告级别超出了本章的范围。他们的相关内容在Ranorex Studio基础知识>报告>[报告级别][1]。


## 配置错误行为
错误是测试的一部分。这就是为什么告诉Ranorex在发生错误时该怎么做很重要。您可以通过在测试套件中配置测试用例和智能文件夹的错误行为来实现。

错误行为在测试用例或智能文件夹的上下文菜单中设置。有四种不同的类型，如下所述。

![A5030-0000120](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5030-0000120.png)      
*错误行为的规范*

>**贴士**   
>默认错误行为是Continue with sibling。

### **继续迭代**

![A5030-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5030-0000090.png)    
*错误行为：继续迭代*

1. 继续迭代
测试运行将继续智能文件夹验证的下一次迭代。

### **继续兄弟**

![A5030-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5030-0000100.png)     
*错误行为：继续兄弟*

1. 继续兄弟

测试测试运行将继续下一个兄弟测试用例或智能文件夹。在我们的例子中，这是智能文件夹 DatabaseCleanUp。

### **继续父母**
![A5030-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5030-0000110.png)     
*错误行为：继续父级*

### **停止**
选择`Stop`错误行为时，错误会立即停止整个测试运行。

### **Setup/teardown区域的错误行为**

设置和拆卸区域遵循特殊的固定错误行为。
- Setup区域中的错误会立即停止测试。
- 如果模块在teardown区域中出现故障，则运行下一个模块。


## 测试套件视图运行测试

![A5030-0000130](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5030-0000130.png)    
*运行测试*

1. 单击`Run`。
2. 观看 Ranorex Studio执行测试。
3. 在测试期间观察进度信息。

>**贴士**   
>单击RUN后，请勿使用键盘或鼠标。这样做会干扰测试操作并导致测试失败。



### **结果：**
 - 一旦测试 跑 完成后，报告出现了。
  
![A5030-0000140](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5030-0000140.png)

>**章节预览**
>Ranorex Studio基础知识>报告>[简介][2]中描述了报告  。

## Ranorex Test Suite Runner
Test Suite Runner是一个独立的程序，可以在没有Ranorex Studio的情况下执行测试套件。当你打开双击Windows中的测试套件文件时，它会自动执行。

您可以使用Ranorex Test Suite Runner来执行整个测试套件，运行某些测试用例和智能文件夹，或者只运行特定模块。

此外，您还可以创建新的运行 配置 与Ranorex Studio相同。

但是，您无法对测试套件本身进行更改。

![A5040-0000150](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5040-0000020.png)

1. 在Windows中，双击测试套件文件。该文件将在Test Suite Runner中打开。

2. 单击`Run`。

1.独立测试套件运行器

2.当前加载的测试套件

---
[👈构建测试][3]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[管理多个测试套件👉][4]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/test-suite/running-tests/#Errorbehavior/

[1]:.\reporting\concept-report-levels-2.html
[2]:.\reporting\introduction.html
[3]:build-a-test.html
[4]:multiple-testsuites.html