# [译] 分析录制

*原文地址 👉 [Analyze a recording][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-29*    

---

在本章中，您将了解有关Recorder工作环境的更多信息，并分析示例测试的录制内容。

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [录制器的工作环境](#录制器的工作环境)
- [动作表分析](#动作表分析)
- [控件库分析](#控件库分析)
- [动作和控件库项之间的链接](#动作和控件库项之间的链接)
- [下载示例解决方案](#下载示例解决方案)  

## 录制器的工作环境

录制器工作环境有四个区域。

### 1. 项目视图

项目视图位于左上角，显示在文件夹层次结构中作为测试项目的一部分创建和管理的所有文件。

![A4040-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4040-0000010.png)  

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> Ranorex Studio \> 👉 [Ranorex Studio起始页][1]章节中介绍了有关内容

### 2. 模块浏览器

模块浏览器位于左下方，它显示了用于构建测试的所有模块和模块组。

![你所访问的页面不存在！(404)](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4040-0000020.png)

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 👉 [测试套件][2]章节中介绍了有关内容

### 3. 动作表

- 您录制的步骤在动作表中显示为动作
- 它们按照执行顺序列出
- 在我们的示例中，列表包含7个动作

![A4040-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4040-0000030.png)  

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 👉 [动作][3]章节中介绍了有关内容

### 4.控件库

- 控件库项表示UI元素
- 受录制期间操作影响的每个UI元素由相应的控件库项引用
- 在我们的示例中，在两个文件夹中组织了五个UI元素

![A4040-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4040-0000040.png)  

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 👉 [控件库][4]章节中介绍了有关内容

## 动作表分析

让我们仔细看看动作表中的七个动作。

![A4040-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4040-0000050.png)  
*示例动作表*  

1. 运行应用动作
    - 该动作在录制开始时启动正在测试的应用程序
2. 鼠标点击动作
    - 该动作表示单击名称文本字段
    - 该动作的最后一列包含对控件库项的引用，该控件库项表示UI元素`EnterYourName`（即名称文本字段）
3. 键盘序列动作
    - 该动作表示输入文本到名称文本字段
    - 在我们的示例中，**Harry**是输入，UI元素`EnterYourName`目标
4. 鼠标点击动作
    - 动作＃4表示单击演示应用程序中的“提交”按钮
    - 提交按钮UI元素在最后一列中由相应的控件库项引用
5. 验证动作
    - 验证操作也表示为一个动作
    - Ranorex将更改后的欢迎消息中的文本与参考文本进行匹配
6. 鼠标点击动作
    - 该动作表示单击`Reset`以重置欢迎消息
7. 鼠标点击动作
    - 最后一个动作表示单击被测应用程序的`Exit`按钮
    - 该动作关闭应用程序

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 👉 [动作][3]章节中介绍了有关内容


## 控件库分析

我们的示例包含组织在两个文件夹中的五个控件库，每个控件库项对应于测试中的应用程序中的UI元素，让我们仔细看看它们。

![A4040-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4040-0000060.png)  

1. 控件库项#1 -- RxButtonExit
    - 该控件库项表示演示程序的`Exit`按钮
2. 控件库项#2 -- EnterYourName
    - 该控件库项表示演示程序的名称文本字段
3. 控件库项#3 -- BtnSubmitUserName
    - 该控件库项表示演示程序的`Submit`
4. 控件库项#4 -- Reset
    - 该控件库项表示演示程序的`Reset`
5. 控件库项#4 -- LblWelcomeMessage
    - 该控件库项表示演示程序欢迎消息的文本标签

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 👉 [控件库][4]章节中介绍了有关内容

## 动作和控件库项之间的链接

录制的动作和控件库项目分别进行管理和存储，但它们相互链接。

![A1060-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A1060-0000030.png)  
*动作和控件库项之间的链接*  

1. 总做引用UI元素

鼠标单击名称文本字段（动作＃2）和输入`Harry`到名称文本字段（动作＃3）都会影响相同的UI元素。因此，它们都链接到表示此UI元素的`EnterYourName`（控件库项＃2）的控件。

2. 表示UI元素的控件库项 

- UI元素表示控件库项
- 控件库项有个名称（例如：`EnterYourName`）和在GUI中的路径

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 动作 \> 👉 [动作和控件库项][5]章节和\> Ranorex Studio 基础教程 \> 控件库 \> 👉 [控件库项和动作][6]章节中对动作和控件库项之间的链接相关内容有说明介绍

## 下载示例解决方案

你可以下载准备好的示例解决方案。  

**示例解决方案** 
> 主题：分析录制
> 时间：10min以内  
> 下载：[点我下载][7]  


**安装**

1. 解压项目目录到你的计算机任一文件夹
2. 使用RanorexStudi打开`Introduction.rxsln`解决方案

**贴士**  
示例解决方案适用于Ranorex版本8.0或更高版本。你需要将解决方案自动升级同意到8.2及更高版本的。



[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/ranorex-recorder/analyzing-recordings/
[1]: ..//..//ranorex-studio-fundamentals/ranorex-studio/ranorex-studio-startpage.html
[2]: ..//..//ranorex-studio-fundamentals/test-suite/introduction.html
[3]: ..//..//ranorex-studio-fundamentals/actions/introduction.html
[4]: ..//..//ranorex-studio-fundamentals/repository/introduction.html
[5]: ..//..//ranorex-studio-fundamentals/actions/[译]动作和控件库项.html
[6]: ..//..//ranorex-studio-fundamentals/repository/[译]控件库项和动作.html
[7]: https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleIntroduction.zip