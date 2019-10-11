# [译] 分析录制



[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月29日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月5日-green.svg?longCache=true&style=flat-square)

---

在本章中，您将了解有关Recorder工作环境的更多信息，并分析示例测试的录制内容。

**本章导视**

- [录制器的工作环境](#录制器的工作环境)
- [动作表分析](#动作表分析)
- [控件库分析](#控件库分析)
- [动作和控件库项之间的链接](#动作和控件库项之间的链接)
- [下载示例解决方案](#下载示例解决方案)  

## 录制器的工作环境

录制器工作环境有四个区域。

### 1. 项目视图

项目视图位于左上角，显示在文件夹层次结构中作为测试项目的一部分创建和管理的所有文件。

![A4040-0000011](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4040-0000011.png)  

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> Ranorex Studio \> 👉 [Ranorex Studio起始页][1]章节中介绍了有关内容

### 2. 模块浏览器

模块浏览器位于左下方，它显示了用于构建测试的所有模块和模块组。

![A4040-0000021](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4040-0000021.png)

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 👉 [测试套件][2]章节中介绍了有关内容

### 3. 动作表

- 您录制的步骤在动作表中显示为动作
- 它们按照执行顺序列出
- 在我们的示例中，列表包含5个动作

![A4040-0000031](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4040-0000031.png)  

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 👉 [动作][3]章节中介绍了有关内容

### 4.控件库

- 控件库项表示UI元素
- 受录制期间动作影响的每个UI元素由相应的控件库项引用
- 在我们的示例中，在两个文件夹中组织了4个UI元素

![A4040-0000041](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4040-0000041.png)  

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 👉 [控件库][4]章节中介绍了有关内容

## 动作表分析

让我们仔细看看动作表中的5个动作。

![A4040-0000051](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4040-0000051.png)  
*示例动作表*  


1. 鼠标点击动作
    - 该动作表示单击名称文本字段
    - 该动作的最后一列包含对控件库项的引用，该控件库项表示UI元素`EnterYourName`（即名称文本字段）
2. 键盘序列动作
    - 该动作表示输入文本到名称文本字段
    - 在我们的示例中，**Harry**是输入，UI元素`EnterYourName`目标
3. 鼠标点击动作
    - 动作＃4表示单击演示应用程序中的“提交”按钮
    - 提交按钮UI元素在最后一列中由相应的控件库项引用
4. 验证动作
    - 验证动作也表示为一个动作
    - Ranorex将更改后的欢迎消息中的文本与参考文本进行匹配
5. 鼠标点击动作
    - 该动作表示单击`Reset`以重置欢迎消息


> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 👉 [动作][3]章节中介绍了有关内容


## 控件库分析

我们的示例包含组织在两个文件夹中的4个控件库项，每个控件库项对应于测试中的应用程序中的UI元素，让我们仔细看看它们。

![A4040-0000061](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4040-0000061.png)  


1. 控件库项#1 -- EnterYourName
    - 该控件库项表示演示程序的名称文本字段
2. 控件库项#2 -- BtnSubmitUserName
    - 该控件库项表示演示程序的`Submit`
3. 控件库项#3 -- Reset
    - 该控件库项表示演示程序的`Reset`
4. 控件库项#4 -- LblWelcomeMessage
    - 该控件库项表示演示程序欢迎消息的文本标签

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 👉 [控件库][4]章节中介绍了有关内容

## 动作和控件库项之间的链接

录制的动作和控件库项目分别进行管理和存储，但它们相互链接。

![A1060-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A1060-0000030.png)  
*动作和控件库项之间的链接*  

1. 动作引用的UI元素

鼠标单击名称文本字段（动作＃1）和输入`Harry`到名称文本字段（动作＃2）都会影响相同的UI元素。因此，它们都链接到表示此UI元素的`EnterYourName`（控件库项＃1）的控件。

2. 表示UI元素的控件库项 

- UI元素表示控件库项
- 控件库项有个名称（例如：`EnterYourName`）和在GUI中的路径

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 动作 \> 👉 [动作和控件库项][5]章节和\> Ranorex Studio 基础教程 \> 控件库 \> 👉 [控件库项和动作][6]章节中对动作和控件库项之间的链接相关内容有说明介绍

> **视频向导**  
> 要了解如何手动将UI元素添加到控件库，并将动作添加到未连接到控件库库项目的录制中去，请观看我们的视频—>[RanorexStudio Recorder基础知识5：手动添加元素和动作][8](视频来自Youtube)

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
>示例解决方案适用于Ranorex版本8.0或更高版本。你需要将解决方案自动升级同意到8.2及更高版本的。

---
[👈录制一个测试][9]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[运行和调试录制👉][10]



[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/ranorex-recorder/analyzing-recordings/
[1]: ..//..//ranorex-studio-fundamentals/ranorex-studio/ranorex-studio-startpage.html
[2]: ..//..//ranorex-studio-fundamentals/test-suite/introduction.html
[3]: ..//..//ranorex-studio-fundamentals/actions/introduction.html
[4]: ..//..//ranorex-studio-fundamentals/repository/introduction.html
[5]: ..//..//ranorex-studio-fundamentals/actions/[译]动作和控件库项.html
[6]: ..//..//ranorex-studio-fundamentals/repository/[译]控件库项和动作.html
[7]: https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleIntroduction.zip
[8]: https://youtu.be/Q7YpwB6Me-c
[9]: .\recording-a-test.html
[10]: .\run-debug-recordings.html