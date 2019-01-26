# [译] 规划你的首个测试 

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月21日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年1月26日-green.svg?longCache=true&style=flat-square)

---

用时：3min

在开始构建测试之前，我们需要考虑我们实际上要做什么。这有助于防止错误和冗长的测试重构。


## 规划

为了规划我们本指南中将要创建的测试，我们将问自己以下问题，当你创建更复杂的测试时，这些也适用。

- 我们想做什么测试
- 我们可以怎么测试它

### 我们想做什么测试

在本指南中，我们将测试Ranorex Studio 演示应用程序，这是一个简单的程序，可以帮助你学习如何使用Ranorex Studio。


**演示应用程序下载**  
>  演示应用程序可以在这里下载 👉 [Ranorex 演示应用程序][1]将应用程序解压缩到你选择的任何文件夹中。出于本指南的目的，我们假设它已保存到系统的/`Downloads`/文件夹中。

![A1040-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1040-0000020.png)  
*演示程序起始页*  

我们将创建一个测试，以确认在`Enter your name`字段中输入的文本在单击`Submit`之后出现在右侧的欢迎消息中。

### 我们可以怎么测试它

为了测试上面描述的行为，我们的测试需要包括以下操作:

1. 启动演示程序
2. 点击文本框
3. 在文本框中输入`Harry`
4. 点击提交
5. 验证在欢迎界面显示的文本
6. 关闭程序

如果所提交的名称出现在欢迎消息中，则测试成功。



[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/ranorex-studio-fundamentals/3-plan-first-test/
[1]: https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxDemoApp.zip