# [译] 运行和调试录制

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月29日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月5日-green.svg?longCache=true&style=flat-square)

---
在本章中，您将学习如何运行和调试录制。

目前，我们将专注于以最简单的形式运行测试录制：一个接一个地执行录制的动作。在更大的测试自动化环境中，运行测试意味着基于不同的用户数据，参数和测试场景集执行迭代。我们将在后面的章节中讨论这个问题。

> **视频向导**  
> 视频“运行并调试测试”将引导您完成本章中的信息。                   
> [立即观看][7](视频来自Youtube)


**本章导视**


- [开启加速模式](#开启加速模式)
- [运行一个录制模块](#运行一个录制模块)
- [运行一个测试用例](#运行一个测试用例)
- [全局运行按钮](#全局运行按钮)
- [运行选项](#运行选项)
- [调试-失败时开启/关闭](#调试-失败时开启关闭)
- [调试-插入一条日志信息](#调试-插入一条日志信息)
- [开启/关闭调试模式](#开启关闭调试模式)
- [下载示例解决方案](#下载示例解决方案)

> **视频向导**  
>要了解如何运行单个录制，运行测试用例或测试套件，在录制中执行各个步骤，并启用Turbo模式或调试模式，请观看我们的视频⇢[RanorexStudio Recorder基础知识4：运行并调试测试][8](视频来自Youtube)
> 
## 开启加速模式

默认情况下，Ranorex Studio在动作之间使用预定义延迟来控制它们重放的速度。 您可以通过将此延迟减少到几乎为零来启用Turbo模式以加快重放速度。

1. 在录制模块工具栏中，单击`Turbo mode`以打开或关闭turbo模式

![A4050-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4050-0000010.png)  
*在Ranorex录制器里的Turbo模式按钮*  

**提示**  
> 在激活的录制模块中，`Turbo模式`将会应用于所有的动作

## 运行一个录制模块

本节演示如何运行单个录制模块

1. 在录制器视图中，点击`RUN`
2. 看到开始运行和进度框
3. 运行完成后，将显示测试报告。

**贴士** 
> 请记住：在测试运行期间请勿触摸鼠标或键盘，否则可能会导致测试失败。

![A4050-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4050-0000020.png)
*运行一个录制模块*  




> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 👉 [报告][1]章节中详细介绍和解释了测试报告的结构、内容。

## 运行一个测试用例

运行单个录制模块通常仅在编辑或排除故障时完成。测试一般基于测试套件视图中的测试用例运行。测试套件是模块化和测试用例管理的中心控制点。

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 测试套件 \> 👉 [介绍][2]章节中详细介绍和解释了测试套件及其用法。

### 切换测试套件视图

有两种方法切换测试套件视图

- a. 在Studio工具栏上，点击`View`查看测试套件按钮
- b. 或者，点击`Introduction.rxtst`标签页(rxtst = Ranorex test suite file)

![A4050-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4050-0000030.png)  
*切换测试套件视图* 

 

**贴士**            
> 示例测试套件具有与测试项目相同的名称:`Introduction`     
> 当前测试套件包含一个默认名称`TestCase`的测试用例    
> 测试用例包含安装和拆卸区域    
> 测试用例包含一个带有默认名称`Recording1`的录制模块    
> 勾选的复选框意味着测试用例将在测试运行期间执行     

### 执行测试用例

1. 在测试套件视图中，点击RUN，将运行全部测试套件。在我们的示例中，测试套件包含一个测试用例，所以只有这个测试用例被执行。
2. 看到运行开始和进度框

 
![A4050-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4050-0000040.png)  
*运行一个测试用例*  

3. 当运行结束，生成报告


![A4050-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4050-0000050.png)  
*测试报告显示运行成功*  

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 报告\> 👉 [介绍][1]章节中详细介绍和解释了测试套件及其用法。

>**视频向导**  
>视频“进度对话框”向您介绍进度对话框提供的实时信息    
>[立即观看][9]        


## 全局运行按钮

您不必在测试套件视图中运行或停止测试套件。您还可以单击Studio工具栏中的全局运行和停止按钮。它们总是可见的，不管您当前的视图如何。

![A4050-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4050-0000060.png)               
*Ranorex Studio工具栏上全局运行和停止按钮*  

## 运行选项

有时候，您不希望运行整个录制，或者您可能希望控制运行，类似于调试计算机程序，如下所述。

1. 切换到录制器视图
2. 右键一个动作，选择一个选择，解释如下

![A4050-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4050-0000070.png)  
*动作4的上下文菜单*  

1. 运行选择项
    - 只运行选择的动作
2. 运行到这儿(不包括选择项) 
    - 从动作1开始运行到所选的动作，但不包括所选的动作 
3. 从这儿运行
    - 在选择的动作处开始运行
4. 从这儿录制(所选之后) 
    - 开始录制，并将所录制的动作添加到所选择的动作和下一个动作之间


## 调试-失败时开启/关闭

当某个动作在测试期间导致异常时，默认动作是测试中止。有时，您可能希望继续运行，这是“失败时继续”选项很有用的地方。

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 动作 \> 👉 [管理动作][3]章节中详细介绍和解释了调试选项`Continue on fail`概念。

## 调试-插入一条日志信息

当测试变得复杂时，向报表添加特殊的日志消息通常很有帮助。

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 报告 \> 👉 [Ranorex标准报告][4]章节中详细介绍了有关概念。

## 开启/关闭调试模式

Ranorex Studio包含一个专门的调试模式，通过在编程代码中设置断点来工作。这是一个专家主题，这就是为什么我们在这里只简单地讨论一下。

![A4050-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4050-0000080.png)  
*Ranorex Studio调试模式*  

1. 开启/关闭调试模式
2. 调试模式要求Ranorex Studio作为管理员运行。如果不是这样，就会出现在管理员模式下重启的提示。

**贴士**  
> 调试模式将Ranorex Studio性能降低约30％

> **章节预览**  
> 在 \> Ranorex Studio 专家教程 \> Ranorex Studio集成开发环境 \> 👉 [调试][5]章节中详细介绍了有关概念。

## 下载示例解决方案

下载我们的示例解决方案，亲自尝试本章中介绍的步骤和选项。

> 主题：运行和调试录制  
> 时间：10min以内  
> 下载：[点我下载][6] 

**安装**

1. 解压项目目录到你的计算机任一文件夹
2. 使用RanorexStudi打开`Introduction.rxsln`解决方案

**贴士**  
示例解决方案适用于Ranorex版本8.0或更高版本。你需要将解决方案自动升级同意到8.2及更高版本的。

---
[👈分析录制][10]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[管理录制模块👉][11]



[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/ranorex-recorder/run-debug-recordings/
[1]: ..//..//ranorex-studio-fundamentals/reporting/introduction.html
[2]: ..//..//ranorex-studio-fundamentals/test-suite/introduction.html
[3]: ..//..//ranorex-studio-fundamentals/actions/managing-actions.html
[4]: ..//..//ranorex-studio-fundamentals/reporting/ranorex-standard-reporting.html
[5]: ..//..//..//ranorex-studio-expert/ranorex-studio-ide/[译]调试.html
[6]: https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleIntroduction.zip
[7]: https://www.youtube.com/embed/WVVlYI2h6jY
[8]: .\https://youtu.be/WVVlYI2h6jY
[9]:https://www.youtube.com/embed/Eke2Ho1-XDg
[10]:.\analyzing-recordings.html
[11]:.\managing-recording-modules.html