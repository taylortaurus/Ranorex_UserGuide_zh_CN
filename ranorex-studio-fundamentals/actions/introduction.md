# [译] 动作

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月6日-green.svg?longCache=true&style=flat-square)

---

动作是由模块执行的单个活动。在Ranorex中，有两种动作：基本动作和智能动作。基本动作表示直接用户输入，例如鼠标单击。智能动作代表更复杂的输入或特殊功能，例如运行浏览器或执行验证。大多数动作都在控件库项目上执行。动作在“录制器”视图的动作表中进行管理。

**本章导视**
- [基本动作](#基本动作)
- [智能动作](#智能动作)
- [动作表中的动作](#动作表中的动作)

>**视频向导**   
>视频“动作简介”将引导您完成本章中的内容。   
[立即观看](https://www.youtube.com/embed/HxBpGTn69Og)（视频来自Youtube）

## 基本动作

基本动作表示在设备上或在设备上的直接用户输入，例如鼠标点击或键盘输入。在录制期间执行这些动作时会自动录制这些动作，但也可以在动作表中手动添加。下表列出了每个基本动作的名称。有关每个基本动作的更多详细信息[👉动作属性][1]。请参阅以下页面：   


	Mouse                   鼠标
	Mouse wheel             鼠标滚轮
	Touch                   触摸
	Swipe gesture           滑动手势
	Key shortcut            关键捷径
	Key sequence            键序列
	Mobile key press        移动按键


## 智能动作
智能动作代表更复杂的UI交互和功能。例如，“Run”应用程序动作直接从特定路径运行可执行文件，而不需要通过鼠标单击或键盘交互来执行此动作。在录制期间，除验证动作外，这些动作都不可用。有关每个智能动作的更多详细信息👉[动作属性][1]，请参阅以下页面：

	Validation              验证
	Invoke action           调用动作
	Get value               获取值
	Set value               设定值
	Open browser            打开浏览器
	Run application         运行应用程序
	Run mobile application  运行移动应用程序
	Deploy Android app      部署Android应用
	Deploy iOS app          部署iOS应用程序
	Set device orientation  设置设备方向
	Close application       关闭应用程序
	Wait for                等待
	Log message             记录消息
	Capture screenshot      捕获截图
	Create snapshot         创建快照
	Separator               分隔器
	Delay                   延迟
	User code               用户代码


## 动作表中的动作
动作在“录制器”视图的动作表中进行管理。

![A6010-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6010-0000030.png)    
*Ranorex Studio动作表*

**注意**   
>动作总是按时间顺序列出，即动作＃4在动作＃5之前执行。

---
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[动作和控件库项目👉][2]


[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/actions/introduction/

[1]:.\action-properties.html
[2]:.\actions-repository-items.html