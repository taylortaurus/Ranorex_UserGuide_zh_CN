# [译] 验证工具提示


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月10日-green.svg?longCache=true&style=flat-square)

---
验证工具提示比验证其他类型的UI元素更具挑战性。在本章中，您将学习如何动作。

**本章导视**


- [测试定义](#测试定义)
- [激活工具提示验证](#激活工具提示验证)
- [验证工具提示](#验证工具提示)
- [结果](#结果)
- [下载示例解决方案](#下载示例解决方案)





>**视频向导**             
视频“工具提示验证”将引导您完成本章中的信息。                    
[立即观看](https://www.youtube.com/embed/rsSBcaPdb_k)

## 测试定义
我们想验证当用户将鼠标悬停在`Shuffle`按钮上时，下图中显示的工具提示正确显示。

![A8070-0000011](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8070-0000011.png)



## 激活工具提示验证
要激活工具提示验证：

![A8070-0000021](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8070-0000021.png)          
*录制器热键激活*

1. 激活启用热键。

>**章节预览**                
Ranorex Studio基础> Ranorex Recorder>  👉[录制器控制中心和热键][1]中介绍了录制器热键。



## 验证工具提示
1. 将光标 放在要验证其工具提示的UI元素上。

2. 出现工具提示时，按 T 键。

![A8070-0000031](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8070-0000031.png)            
*指定工具提示验证*

3. 在下一个屏幕中，检查是否已选择正确的工具提示元素，然后单击“Next”进行确认。

4. 确保选中“Exists”属性，然后单击“确定”进行确认。
指定工具提示验证


## 结果
动作表中有两个录制的动作。动作＃2是工具提示验证。

![A8070-0000051](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8070-0000051.png)          
*工具提示验证结果*

1. 动作表和工具提示验证动作。

2. 表示工具提示UI元素的链接控件库项。



## 下载示例解决方案
您可以在此处下载本章的示例解决方案。它包含已完成的所有录制动作的解决方案。


**示例解决方案**
>主题：工具提示验证
>时间：15分钟           
>[点我下载](https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleTooltipValidation.zip)

### **安装示例解决方案：**
1. 解压缩到计算机上的任何文件夹。

2. 启动 Ranorex Studio并打开解决方案文件TooltipValidation.rxsln

>**贴士**          
样本解决方案适用于Ranorex Studio 8.0或更高版本。您必须同意8.2及更高版本的自动解决方案升级。


---

[👈基于图像的验证示例][2]



[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/test-validation/validation-tool-tips/
[1]:.\ranorex-recorder\recorder-hotkeys.html
[2]:.\image-based-validation-example.html