# [译] 分析你的录制动作
 

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月21日-green.svg?longCache=true&style=flat-square)


---

用时：3min

每次录制后，分析录制的动作和生成的**控件库**库项目，以及它们的连接方式，这有助于防止错误。

**本章导视**

- [录制的动作](#录制的动作)
- [控件库项](#控件库项)
- [在动作和控件库项之间的连接](#在动作和控件库项之间的连接)

## 录制的动作

录制视图中的表包含6个单独的，相应编号。让我们仔细看看它们。

![A1060-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1060-0000010.png)

1. 动作#1 -- 运行应用
    - 该动作是启动Ranorex演示程序 
2. 动作#2 -- 鼠标点击
    - 该动作在`EnterYourName`文本框中执行单击
3. 动作#3 -- 键值序列
    - 该动作在`EnterYourName`文本框输入`Harry`
4. 动作#4 -- 鼠标点击
    - 该动作是单击**Submit**，使用在步骤3中输入的名称更新欢迎消息
5. 动作#5 -- 验证
    - 该动作验证欢迎消息是否已正确更新
6. 动作#6 -- 鼠标点击
    - 该动作单击**Exit**，关闭演示应用程序 

**贴士**  
> 如果你没有准确地遵循录制说明进行操作，则可能会有额外的录制动作。如果是，请确定不属于预期测试的并将其删除。

**注意**  
> 关于验证 - 验证输入键序列是否与验证参考文本序列完全匹配！验证区分大写字母和小写字母。

## 控件库项

上面列出的一些动作操纵UI元素。这些UI元素表示为控件库中的控件库项目，它出现在录制视图的下半部分。

![A1060-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1060-0000020.png)  

1. 控件#1 -- `RxButtonExit`
    - 该控件表示**Exit**按钮
2. 控件#2 -- `EnterYourName`
    - 该控件表示文本框`EnterYourName `
3. 控件#3 -- `BtnSubmitUserName`
    - 该控件表示**Submit**按钮
4. 控件#4 -- `LblWelcomeMessage`
    - 该控件表示欢迎辞文本

## 在动作和控件库项之间的连接

操纵UI元素的动作（例如单击按钮）会自动链接到相应的控件库项中的控件，控件库项显示在动作表中的动作旁边，单击该动作时，该项目也会在控件库中突出显示。
不操纵UI元素的动作（例如启动应用程序）不会链接到控件库项。

![A1060-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Ranorizeyourselfin20minutes/A1060-0000030.png)

1. 操作EnterYourName文本框的动作
    - “Mouse”动作会在文本框中执行鼠标单击。“Key sequence”动作则在文本框中输入Harry。这两个动作都链接到名为EnterYourName控件库项

2. 表示受操纵的UI元素的控件库项

---
[👈录制你的首个测试][1]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[运行测试并检查报告👉][2]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/ranorex-studio-fundamentals/5-analyze-recording/

[1]: .\4-record-first-test.html
[2]: .\6-run-test-check-report.html