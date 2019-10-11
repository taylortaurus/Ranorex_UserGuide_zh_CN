# [译] 创建控件库项目

*原文地址 👉 [Create repository items][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2019-9-9*    

---

在本章中，您将了解创建控件库项目并将其添加到控件库的各种方法。


**本章导视**


- [录制期间自动创建](#录制期间自动创建)
- [使用“Track”按钮创建控件库项目](#使用“Track”按钮创建控件库项目)
- [使用即时跟踪创建控件库项目](#使用即时跟踪创建控件库项目)
- [使用Ranorex Spy创建控件库项目](#使用RanorexSpy创建控件库项目)
- [在控件库中手动创建一个控件库项目](#在控件库中手动创建一个控件库项目)

>**视频向导**    
视频“创建控件库项目”将引导您完成本章中的内容。        
[立即观看](https://www.youtube.com/embed/6wGrTlKXaZs)

## 录制期间自动创建
当您使用Ranorex Recorder录制测试并对UI元素执行动作时，将创建相应的控件库元素并自动添加到控件库中。

![A7030-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7030-0000010.png)         
*在录制期间自动创建的控件库项目*


## 使用“Track”按钮创建控件库项目

Track按钮在控件库视图和Ranorex Spy中可用。使用此按钮可以手动跟踪UI元素并创建控件库项目。当您需要更新已更改的UI元素的定义时，这尤其有用。

>**贴士**   
关于使用“Track”按钮将在下面详细说明   
Ranorex Studio高级>跟踪UI元素>👉[Track按钮][1]

## 使用即时跟踪创建控件库项目
即时跟踪是手动创建控件库项目的另一种方法。这对于手动识别不易访问的UI元素（如下拉菜单中的项目）尤其有用。要激活即时跟踪，请将鼠标悬停在所需的UI元素上，然后按快捷键Ctrl + WIN  。

>**贴士**        
关于使用即时跟踪将在下面详细说明        
Ranorex Studio高级>跟踪UI元素>👉[即时跟踪][2]。

## 使用Ranorex Spy创建控件库项目
您还可以从Ranorex Spy手动添加控件库项目，Ranorex Spy是一种用于映射和识别UI元素的专用工具。

>**章节预览**    
Ranorex Spy在 Ranorex Studio高级>👉[RanorexSpy][3]中介绍RanorexSpy。

## 在控件库中手动创建一个控件库项目
最后，您可以在控件库视图本身中手动创建控件库项。

为此：

1. 右键单击应用程序文件夹，有根文件夹或简单文件夹。

2. 单击Add new iteam>Iteam。

3. 手动跟踪项目的路径并为其命名。

>**贴士**    
以下章节讲述了用于识别控件库项的RanoreXPath    
Ranorex Studio高级> RanoreXPath>👉[简介][4]

---

[👈控件库项目和动作][5]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[管理控件库项目👉][6]







[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/repository/creation-repository-items/
[1]: .\ranorex-studio-advanced\tracking-ui-elements\introduction.html
[2]: .\ranorex-studio-advanced\tracking-ui-elements.html
[3]: .\ranorex-studio-advanced\ranorex-spy\introduction.html
[4]: .\ranorex-studio-advanced\ranorexpath\introduction.html
[5]: .\repository-items-actions.html
[6]: .\managing-repository-items.html