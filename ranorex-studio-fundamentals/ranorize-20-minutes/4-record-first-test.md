# [译] 录制你的首个测试

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月21日-green.svg?longCache=true&style=flat-square)



---

用时：6min

是时候录制我们的测试了!这意味着我们将手动执行我们在上一章中确定的动作，并让Ranorex Studio录制它们。

**本章导视**

- [成功录制的步骤](#成功录制的步骤)
- [选择应用开始录制](#选择应用开始录制)
- [录制测试](#录制测试)
- [验证UI元素](#验证ui元素)
- [退出应用并停止录制](#退出应用并停止录制)
- [总结](#总结)

## 成功录制的步骤

Ranorex Studio支持各种环境，测试规范和技术设置。 因此，无论你的环境如何，你的首次录制都是成功的，我们建议你执行以下动作：

- 录制时，只使用鼠标进行导航
    - 避免使用其他输入设备，如图形平板电脑，触摸板，笔
- 点击每一步骤
    - 不要使用Tab键浏览表单
- 关闭提前应用
    - 关闭你不需要进行测试的任何其他应用程序或工具
- 在另一台计算机上打开用户指南
    - 如果可能，请在另一台计算机或平板电脑上打开用户指南，以便在录制测试时参考
- 单击录像机中的暂停/继续
    - 要查看用户指南或执行你不想操作的动作，只需单击录制器控制中心中的暂停按钮
- 将显示缩放设置为100％
    - 在Windows显示设置中，将所有显示的显示比例设置为100％。

## 选择应用开始录制

1. 单击录制视图中的`RECORD`按钮
2. 在打开的对话框中单击`Desktop`

![A1050-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1050-0000010.png)  

3. 在下一个窗口中，单击`Add app...`
4. 打开保存Ranorex演示应用程序的位置，例如 你的计算机的/`Downloads`/文件夹。
5. 在该文件夹中，选择`RxDemoApp.exe`并单击`Open`，选择Ranorex演示应用程序作为测试应用程序。

![A1050-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1050-0000020.png)  

**注意**  
> 不要单击`录制`按钮。 点击它后，将录制`所有按键和大多数用户交互`。首先阅读下一节，然后执行其中的说明。

## 录制测试

1. 单击`Record`按钮开始录制。Ranorex Studio自动切换到演示应用程序，录制器控件出现。

![A1050-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1050-0000030.png)  

2. 单击**Enter your name**文本字段，输入**Harry**，然后单击**Submit**。

![A1040-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1040-0000030.gif)  

## 验证UI元素

我们可以看到Harry出现在欢迎辞中。现在我们将添加一个**验证**，以便Ranorex Studio在测试期间验证这一点。

1. 单击录像机控件中的**Validate**以暂停录制并切换到验证模式。

![A1050-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1050-0000040.png)  

2. 将鼠标**悬停**在欢迎消息上，出现**紫色框**，这意味着已经识别了**UI元素**，点击它。

![A8030-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A8030-0000010.gif)  

3. **选择元素**窗口打开。**检查**右下角的**屏幕截图**是否显示要验证的UI元素。在我们的例子中，这就是欢迎信息。单击**Next**确认。

4. 打开验证设置窗口。在这里，你可以选择要验证的属性。在我们的例子中，text是正确的预选择。单击**OK**确认并切换回录制模式。

![A1050-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1050-0000060.png)  

## 退出应用并停止录制

1. 单击演示应用程序右下角的**Exit**将其关闭。

2. 单击“录制器”控件中的**Stop**以停止录制。

![A1050-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1050-0000070.png)  

## 总结

下图显示了本章中描述的所有录制步骤。你可以在录制时将其用作屏幕辅助。

![A1050-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1050-0000080.png)


---
[👈创建一个新的解决方案][1]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[分析你的录制动作👉][2]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/ranorex-studio-fundamentals/4-record-first-test/
[1]:.\2-create-new-solution.html
[2]:.\5-analyze-recording.html
