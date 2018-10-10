# [译] Ranorex 录制器

*原文地址 👉 [Ranorex Recorder][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-7-8*    
*♋ update time : 2018-9-26*  

---

Ranorex Recorder允许你记录用户界面测试所需的键盘和鼠标操作。这些操作显示在Recorder的动作表中，你可以在其中编辑或添加更多操作。这样，你就可以创建录制以满足你的测试需求。Ranorex Recorder可作为Ranorex Studio中的集成工具使用，也可作为独立版本使用。


**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [集成录制](#集成录制)
- [独立录制](#独立录制)
- [集成录制 vs 独立录制](#集成录制%20vs%20独立录制)

## 集成录制

当你开始一个新的测试项目时，工作环境将显示一个空的记录模块被打开。

![A4010-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4010-0000010.png)  
*集成录制*  

1. 激活`Recording1.rxrec`录制模块
2. 集成录制器控制面板

## 独立录制

Ranorex还提供独立的录制器。它可以独立于Ranorex Studio启动。

![A4010-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4010-0000020.png)  
*独立录制器*  

1. 打开Windows开始菜单
2. 点击`Ranorex` > `Ranorex Recorder 8`
3. 按照需求（32位或是64位）启动独立录制器

## 集成录制 vs 独立录制

两种版本的录制器基本功能都相同。但是独立录制器器具有较少的功能。这就是我们建议你使用集成记录器的原因。

一个主要的区别是独立的录制器不允许用户代码操作（这在自动化测试中很流行），独立的Recorder默认情况下也使用嵌入式控件库。在处理更复杂的测试任务时，这可能会受到限制。

出于这些原因，“用户指南”侧重于集成的录制器器。


[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/ranorex-recorder/introduction/
[1]: ..\\..\\Ranorize_yourself_in_20_minutes/index.html
[2]: https://www.ranorex.com/blog/studio-quick-start/

