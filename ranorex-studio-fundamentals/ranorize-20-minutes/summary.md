# [译] 总结

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-Taylortaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月6日-green.svg?longCache=true&style=flat-square)
---

恭喜你!你刚刚用Ranorex Studio完成了你的第一个自动化软件测试。

如果你想要更多的测试动作，请继续尝试下面关于导致测试失败的简短教程。

或者，简单地翻到页面底部，就如何在Ranorex Studio度过你的下一个小时提出建议。

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [创建一个失败的测试](#创建一个失败的测试)
- [你和Ranorex的下一个小时](#你和ranorex的下一个小时)

## 创建一个失败的测试

测试失败是测试的一部分。 让我们在受控的环境中制作一个，看看它们在Ranorex Studio中的样子。

1. 要返回录制视图，请单击`Recording1.rxrec`选项卡

![A1080-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1080-0000010.png)

1. 选择动作#3并将文本输入更改为`Sally`  

![A1080-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1080-0000020.png)

3. 返回测试套件视图并运行测试
   
4. 测试失败，报告显示发生了什么

![A1080-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1080-0000030.png)  
*失败的测试报告*  

测试失败，因为欢迎消息的验证失败，验证期望值“Welcome, Harry!”，但它实际上找到了值“Welcome, Sally!”，因此，测试中止。


## 你和Ranorex的下一个小时

对于Ranorex的下一个小时，我们建议你查看下面列出的用户指南Ranorex Studio基础部分的第一章。

### Ranorex Studio

Ranorex Studio是在统一界面中组织Ranorex功能的中央平台。在本章中，你将：

- 获得起始页面的概述
- 学习如何创建和启动新的解决方案
- 并熟悉Ranorex Studio用户界面的主要组件

> **章节预览**  
> 跳转到 \> Ranorex Studio 基础教程 \> Ranorex Studio \> 👉 [RanorexStudio起始页][1]

### Ranorex 录制器

录制是你录制测试的地方，在这一章中，你会发现关于以下主题的详细信息:

- 录制测试
- 分析录制
- 并设置运行和调试选项

> **章节预览**  
> 跳转到 \> Ranorex Studio 基础教程 \> Ranorex录制器 \> 👉 [介绍][2]

### 测试套件

测试套件是你管理、结构和模块化测试用例和测试模块的地方。在这一章中，你会发现关于以下主题的详细信息:

- 测试套件的结构和元素
- 模块化
- 建立复杂的测试

> **章节预览**  
> 跳转到 \> Ranorex Studio 基础教程 \>  👉 [测试套件][3]

---
[👈运行测试并检查报告][4]



[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/ranorex-studio-fundamentals/summary/
[1]: ..//..//ranorex-studio-fundamentals/ranorex-studio/ranorex-studio-startpage.html
[2]: ..//..//ranorex-studio-fundamentals/ranorex-recorder/introduction.html
[3]: ..//..//ranorex-studio-fundamentals/test-suite/introduction.html
[4]: .\6-run-test-check-report.html