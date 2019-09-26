# [译] 你开始录制之前


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月27日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月5日-green.svg?longCache=true&style=flat-square)

---

无论您的测试是简单还是复杂，准备工作都是测试自动化的关键。从长远来看，准备工作可以防止错误并节省时间。本章介绍开始录制测试之前要采取的步骤。

**本章导视**

- [录制建议](#录制建议)
- [我们的待测应用--Ranorex演示程序](#我们的待测应用--ranorex演示程序)
- [录制规划](#录制规划)
- [测试定义](#测试定义)
- [录制器默认设置](#录制器默认设置)

## 录制建议

花点时间考虑以下建议。 它们可以使您的测试生活更轻松，您的工作更有效率。

|名称|解释|
|:--|:--|
|Application under test (AUT)|您是想每次都自己启动AUT，还是希望Ranorex在录制开始时自动启动它？ 在任何一种情况下，您都需要知道安装路径和任何所需的启动参数|
|Test data & parameters|确保您拥有可用于测试的所有测试数据和参数，例如登录名和密码|
|Test instances|在录制期间仅运行一个AUT实例|
|Recording interaction|在录制期间捕获所有用户动作，甚至是与AUT无关的意外动作。 确保禁用任何可能干扰录制的内容，例如弹出窗口|
*录制建议*  

> **章节预览**  
> 白名单可以确保Ranorex仅与您的测试相关的过程进行交互。在 \> Ranorex Studio 基础教程 \> 👉 [白名单][1]章节中了解详情


## 我们的待测应用--Ranorex演示程序

为了更好地演示本用户指南中的概念和方法，我们创建了一个特殊应用程序--Ranorex演示应用程序。它将作为我们的AUT，用于本用户指南的基础和高级章节中的解释和示例。

### 下载演示程序

> 在这下载最新版的演示程序 [👉 Ranorex Demo Application][5]在你的系统上解压到任一目录。出于我们教程的目的，我们假设它位于/ Downloads /文件夹中

![A4020-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4020-0000020.png)  
*演示应用程序放在默认目录*  

**提示**  
> 在本用户指南的基础和高级章节中，所有可下载的示例解决方案都包含演示应用程序的链接。

### 启动ATU

在详细规划测试之前，请启动AUT以确保其安装正确且正常工作。

1. 打开保存目录并解压文件
2. 双击打开

![A4020-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4020-0000030.png)
*打开的Ranore Demo Application*  

3. 出现演示程序的欢迎界面

## 录制规划

规划你的录制。它有助于防止繁琐的重组和编辑。

### 使用录制脚本

- 想好你需要录制的步骤
- 准备好必要的录入数据（用户名，密码等）
- 在没有录制时，至少进行一次手动测试

### 考虑录制的大小

- 使录制尽可能的小
- 更大、模块化的测试用例可以用较小的、可重复使用的录制构建

### 计划如何录制鼠标移动

- 默认情况下，**不点击鼠标就不会录制鼠标移动**。
- 当在菜单中导航对于测试很重要时，可以使用鼠标单击进行检测，或者在录制器器控制中心中使用录制鼠标移动的选项。


> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> Ranorex Recorder \> 👉 [录制器控制中心&热键][2]章节中详细介绍和解释了`UI元素`的高级概念

## 测试定义

根据上述建议，我们已经定义了一个简单的测试，包括五个步骤。这个相同的测试在即将到来的Ranorex Recorder章节中作为一个例子。

1. 打开Ranorex演示程序
2. 在`Enter your name`区域输入`Harry`并点击`Submit`

![A1040-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A1040-0000030.gif)  

3. 验证欢迎信息是否相应更改
4. 重置欢迎信息
5. 关闭演示应用程序并停止录制

## 录制器默认设置

您可以配置一些设置来自定义录制器的动作。默认设置通常适用于大多数录制任务，包括本章中的任务。但是对于某些录制任务，您可能需要更改录制器设置。要访问它们，请单击Recorder工作环境工具栏或Ranorex Studio工具栏中的“设置”。

![A4020-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4020-0000040.png)  
*全局&本地录制器设置*  

1. 全局录制器设置
2. 本地录制器设置只对当前录制模块生效

> **章节预览**  
> 在 \> Ranorex Studio 系统详情 \> 设置和配置 \> 👉 [Ranorex录制器设置][3]章节中可以了解录制器设置及其对录制的影响

---
[👈介绍][4]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[录制一个测试👉][6]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/ranorex-recorder/before-you-start-recording/
[1]: ..//..//ranorex-studio-fundamentals/whitelisting/whitelisting.html
[2]: ./recorder-hotkeys.html
[3]: ..//..//..//ranorex-studio-system-details/settings-configuration/[译]Ranorex录制器设置.html
[4]: .\introduction.html
[5]:https://www.ranorex.com/rx-media/rx-user-guide/v8.2/download/RxDemoApp.zip
[6]:.\recording-a-test.html

