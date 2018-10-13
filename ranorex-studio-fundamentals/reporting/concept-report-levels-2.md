# [译] 报告等级

*原文地址 👉 [Report levels][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-21*    

---

报告级别对测试运行期间发生的事件进行分类，并控制报告中包含哪些信息。当你的测试包含数百个带有数千个模块的测试用例时，报告级别是在细节和简洁之间取得平衡的关键。在本章中，你将了解报表级别是如何工作的以及如何使用它们。

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [下载示例解决方案](#下载示例解决方案)
- [有哪些报告级别]()
- [提高注意力]()
- [报告确认]()
- [设置识别级别]()
- [应用示例]()

## 下载示例解决方案

本章内容基于你在下面下载的示例解决方案。

**解决方案** 
> 主题：构建一个测试
> 时间：15min以内  
> 下载：[点我下载][1]  

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/reporting/concept-report-levels/
[1]: https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleIntroduction.zip

### 安装示例解决方案

**安装**

1. 解压项目目录到你的计算机任一文件夹
2. 使用RanorexStudi打开`RxDatabase.rxsln`解决方案

**贴士**  
示例解决方案适用于Ranorex版本8.0或更高版本。你需要将解决方案自动升级同意到8.2及更高版本的。


## 有哪些报告级别

Ranorex Studio提供6个默认报告级别，每个级别都有相应的颜色和整数值。

![A9030-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9030-0000010.png)  
*默认Ranorex报告级别*  

- 报告级别的整数值越高，其关注级别越高，即调试通知引起的关注程度低于信息通知
- 在录制模块中，默认报告级别适用
- 在代码模块中，你可以定义自己的报告级别

## 提高注意力

报告级别的概念很容易解释，这是提高注意力和被认可之间的相互作用。让我们从一个简单的例子开始吧，执行的操作，成功或失败的测试验证以及插入的用户定义的日志消息通过将专用报告级别附加到其状态信息来提高测试运行期间的报告注意力。

![A9030-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9030-0000020.png)  
*按报告级别提高报告关注度的动作*  

1. 操作#1-#4和#6-#7具有报表级别信息(值= 20)。

2. 实际上，验证要么成功，要么失败。因此，成功的测试验证(操作#5)具有报告级别的成功(值= 110)。如果它失败了，它将有报告级别的失败(值= 120)。

## 报告确认

报告消息的识别由测试套件结构元素控制。测试套件、测试用例和智能文件夹设置识别级别，以控制在当前报告中包含哪些状态消息。

**贴士**  
> 识别级别充当可见性障碍——每个带有类似于识别级别或以上的报告级别的状态消息都包含在当前报告中。

### 识别等级--信息（值=20）

[A9030-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/raw/master/Reporting/A9030-0000030.png)

1. 识别等级设置为`Info`（值=20）
2. 只包括所有带有报告级别信息和以上信息的状态消息

### 识别等级--成功（值=110）

![A9030-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9030-0000040.png)  

1. 识别等级设置为`Success`（值=110）
2. 只有状态成功的测试验证(值= 110)包含在报告中

## 设置识别级别

在所有的测试套件结构元素中，作为状态消息进入报表的入口障碍的识别级别都受到控制。测试套件、测试用例和智能文件夹以自顶向下的方式定义它们的报表识别级别。

1. 更改测试套件视图
2. 右键测试套件、测试用例或是智能文件夹
3. 点击报告级别并选择想要的值

![A9030-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9030-0000050.png)  

1. 继承

选择此选项后，报表级别将直接继承父级结构化项目。

## 应用示例

让我们将上述解释应用于一个例子。 我们将插入一条日志消息并设置其报告级别。

### 初始状态

示例解决方案中的记录模块包含7个记录的操作，其中一个是验证操作。

测试用例的识别级别设置为Success。这意味着目前只有在测试运行期间才会报告成功或失败的验证。

我们现在想要添加一条日志消息，告诉我们已单击“提交”按钮，当然我们希望它显示在报告中，而除了验证之外的所有其他操作都不应显示。

### 如何操作

1. 在动作#4后面添加一条日志信息

![A9030-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9030-0000060.png)  

2. 输入消息并将其报告级别设置为“Success”。

### 结果

录制动作的报告级别和测试用例的识别级别现在看起来是这样的:

![A9030-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9030-0000070.png)  
*示例应用的测试报告*  

1. 日志消息，报告级别成功。

2. 测试验证成功，报告级别成功。
