# [译] 录制一个测试


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月28日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月5日-green.svg?longCache=true&style=flat-square)

---

在本章中，您将学习如何录制测试并熟悉基础自动化概念。

**本章导视**

- [成功录制的步骤](#成功录制的步骤)
- [录制测试](#录制测试)
- [验证测试](#验证测试)
- [完成并结束录制](#完成并结束录制)
- [下载示例解决方案](#下载示例解决方案)

## 成功录制的步骤

Ranorex Studio支持各种环境，规格和设置。无论您的环境如何，为了使您的首次录制成功，我们建议您执行以下动作：

- **录制时，只使用鼠标进行导航**

    - 避免使用其他输入设备，如图形平板电脑，触摸板，笔等

- **点击每一步骤**

    - 不要使用Tab键浏览表单

- **关闭其他应用程序**

    - 关闭您不需要进行测试的任何其他应用程序或工具

- **在其他机器上打开用户手册**

    - 如果可能，请在另一台计算机或平板电脑上打开用户指南，以便在录制测试时参考

- **在录制器中点击暂停/继续**

    - 要查看用户指南或执行您不想录制的动作，只需单击录制器控制中心中的暂停按钮

- **将显示缩放设置为100％**

    - 在Windows显示设置中，将所有显示器的显示比例设置为100％





## 录制测试

**贴士**  
> 请记住，如果您不使用白名单，则一旦开始录制，即使未在AUT上执行，也会捕获所有用户交互
> 
> - 点击`Pause`暂停录制，点击`Continue`恢复录制
> - 点击`Stop`终止录制
> 
> 在 \> Ranorex Studio 基础教程 \> Ranorex 录制器 \> 👉 [Ranorex控制中心&热键][1]章节中了解关于录制器控制中心的相关内容
>
> 在 \> Ranorex Studio 基础教程 \> 👉 [白名单][2]章节中了解白名单相关内容

1. 点击`Record`开始录制，Ranorex Studio自动最小化到任务栏，录制器控制器中心显示录制激活

![A1050-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A1050-0000020.png)  
*开始录制*  

2. 待测应用程序成为焦点
3. 在文本区域，输入`Harry`并点击`Submit`

![A1040-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A1040-0000030.gif)

## 验证测试

我们已经录制了UI交互。现在是时候验证交互是否导致了期望的结果，即欢迎消息是否相应地改变了。

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 测试验证 \> 👉 [介绍][3]章节中解释了测试验证的概念


1. 点击`Validate`，录制暂停并切换到验证模式

![A1050-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A1050-0000030.png)  
*激活测试验证*  

2. 选择要验证的UI元素：
    - 将鼠标悬停在更改的欢迎消息上鼠标移动后会出现紫色框架
    - 紫色框表示当前选择哪个元素进行验证
    - 一旦选择的内容与欢迎消息匹配后，单击它

![A8030-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A8030-0000010.gif)  
*选择要验证的元素*  

3. 确认UI元素后，点击`Next`
4. 选择验证属性：
    - `Text`和`Visible`是基于文本的验证的默认验证属性，不需要其他属性 。
    - 确认选择后，点击OK

![A1050-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A1050-0000060.png)
*确认元素和选择的属性*  

## 完成并结束录制

完成验证动作后，Ranorex会自动继续录制。下一步是完成并结束测试录制。

1. 点击`Reset`重置欢迎信息到初始状态
2. 在录制控制中心，点击`Stop`终止录制

![A4030-0000041](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4030-0000041.png)  
*完成并结束录制*  

### 结果

录制结束，然后返回“录制器”视图。如果您完全按照说明动作，则应该看到5个录制的动作和4个已识别的UI元素，组织在两个文件夹中，如下所示。

![A4030-0000051](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4030-0000051.png)  
*录制器视图中的录制结果*  


## 下载示例解决方案

您可以根据本章中的说明构建自己的测试解决方案。或者也可以下载准备好的示例解决方案。  

**示例解决方案** 
> 主题：录制一个测试              
> 时间：10min以内  
> 下载：[点我下载][5]  


**安装**

1. 解压项目目录到你的计算机任一文件夹
2. 使用RanorexStudi打开`Introduction.rxsln`解决方案

**贴士**  
>示例解决方案适用于Ranorex版本8.0或更高版本。你需要将解决方案自动升级同意到8.2及更高版本的。

---
[👈你开始录制之前][6]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[分析录制👉][7]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/ranorex-recorder/recording-a-test/
[1]: ./[译]录制器控制中心和热键.html
[2]: ..//..//ranorex-studio-fundamentals/whitelisting/introduction.html
[3]: ..//..//ranorex-studio-fundamentals/test-validation/introduction.html
[4]: ..//..//ranorex-studio-fundamentals/test-validation/[译]验证的概念.html
[5]: https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleIntroduction.zip
[6]:.\before-you-start-recording.html
[7]:.\analyzing-recordings.html


