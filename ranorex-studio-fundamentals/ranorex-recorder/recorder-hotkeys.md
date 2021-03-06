# [译] 录制器控制中心和热键


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年10月11日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月5日-green.svg?longCache=true&style=flat-square)

---

在本章中，您将学习如何有效地使用Recorder控制中心和热键。

**本章导视**

- [最大/最小化视图](#最大最小化视图)
- [标准功能](#标准功能)
- [在录制器中添加/删除动作](#在录制器中添加删除动作)
- [启用/关闭热键](#启用关闭热键)
- [验证模式热键](#验证模式热键)
- [鼠标移动热键](#鼠标移动热键)
- [工具提示验证热键](#工具提示验证热键)
- [基于图像录制的热键](#基于图像录制的热键)
- [更改识别级别](#更改识别级别)

## 最大/最小化视图

录制器控制中心在最大化和最小化的视图中都可用。通过单击窗口右上角的按钮在它们之间切换。

![A4070-0000011](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4070-0000011.png)  

1. 显示所有控件的完整视图和显示最后四个录制动作的动作表
2. 最小化视图，仅显示底部功能区中的控件

## 标准功能

录制器控制中心有三个激活的按钮控件

![A4070-0000021](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4070-0000021.png) 
*录制器控制中心激活的按钮控件*  

1. 验证模式
    - 在录制中插入一个测试验证动作
2. 暂停/继续
    - 暂停/继续录制
    - 暂停时候不会录制用户交互
3. 停止
    - 停止录制
    - 返回Ranorex Studio   

## 在录制器中添加/删除动作

在完整视图中，控制中心显示最后四个录制的动作。从那里，你可以删除它们或查看它们各自的截图

![A4070-0000031](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4070-0000031.png)  

1. 列表显示最后四个录制的动作
2. 将鼠标放在眼睛上方以显示动作的屏幕截图
3. 单击垃圾箱以删除动作

您还可以通过单击控制中心右下角的`Add`来添加三种动作类型中的一种

![A4070-0000041](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4070-0000041.png)  

4. 单击`Add`直接添加三种动作类型之一。在您执行此动作时录制暂停

![A4070-0000051](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4070-0000051.png)  

5. 可用的动作是消息，屏幕截图和延迟。有关这些功能的更多信息，请参阅 👉 [动作属性][1]章节内容

6. 您可以在此处配置所选动作。根据动作而变化。

7. 单击此按钮可添加动作并恢复录制


## 启用/关闭热键

通过将相应的开关设置为打开或关闭来打开和关闭热键

![A4070-0000061](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4070-0000061.png)  

1. 切换到打开和关闭热键
2. 将鼠标悬停在此信息元素上以显示可用的热键

**提示**  
> 启用热键时，您将无法在录制中使用热键字符（`v`，`m`，`t`，`i`），例如输入文字。大写字符`V`，`M`，`T`，`I`可以正常使用


## 验证模式热键

按键盘上的`V`激活验证模式，方法与点击验证按钮相同

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 👉 [测试验证][2]章节中详细介绍和解释相关概念

## 鼠标移动热键

通常，不录制鼠标移动。如果需要录制鼠标移动，可以按`M`键进动作作。按照以下说明练习录制鼠标移动
*录制鼠标移动*  

![A4070-0000071](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4070-0000071.png)

1. 将鼠标移到“简介”选项卡上，然后按`M`键
2. 将鼠标移到名称文本字段上，然后按`M`键
3. 将鼠标移到“提交”按钮上，然后按`M`键
4. 将鼠标移到“退出”按钮上，然后按`M`键

### 结果

一旦停止录制，动作表将列出四个鼠标移动的动作。每个动作都链接到UI元素。

![A4070-0000081](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4070-0000081.png)    
*录制的鼠标移动*  


## 工具提示验证热键

按`T`开始工具提示验证

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 测试验证 \> 👉 [验证工具提示][3]章节中详细介绍和解释相关概念


## 基于图像录制的热键

按`I`激活基于图像的录制

> **章节预览**  
> 在 \> Ranorex Studio 高级教程 \> 👉 [基于图像的自动化][4]章节中详细介绍和解释相关概念


## 更改识别级别

激活热键时，鼠标滚轮控制UI元素检测的识别级别。我们来看一个简单的例子吧。

### 初始的识别级别：

- Ranorex Recorder在录制期间识别每个UI元素
- UI元素识别通过录制期间鼠标移动后的红框可见

![A4070-0000091](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4070-0000091.png)  
*红框的UI元素*  

### 更改识别级别：

滚动鼠标滚轮以在UI元素级别中移动

![A4070-0000101](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4070-0000101.png)  
*滚动鼠标滚轮时，识别级别会发生变化*

---
[👈管理录制模块][5]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/ranorex-recorder/recorder-hotkeys/
[1]: ..//..//ranorex-studio-fundamentals/actions/action-properties.html
[2]: ..//..//ranorex-studio-fundamentals/test-validation/introduction.html
[3]: ..//..//ranorex-studio-fundamentals/test-validation/validation-tool-tips.html
[4]: ..//..//..//ranorex-studio-advanced/image-based-automation/introduction.html
[5]:.\managing-recording-modules.html


