# [译]基于图像的自动化--介绍

*原文地址 👉 [Image-based automation][0]*

*@translator : [TaylorTaurus](https://github.com/taylortaurus)*  
*translate time : 2018-7-5*

---

自动化软件测试通常基于对用户界面元素(ui元素)的识别。它们中的许多可以根据文本进行识别。
另外，测试自动化还需要识别像素图像而不是文本。基于图像的自动化是一种很好的识别、检测和应用ui元素的方法。本文介绍并解释了使用这种方法所需要的一切。

本章节有如下内容：

- 解决方案示例
- 开启/关闭基于图像的自动化
- 为什么需要基于图像的自动化

## 解决方案示例

本文介绍的概念放在一个示例解决方案中，可以下载。我们邀请您使用示例解决方案进行实验，并提升您的认知。

> **训练！你可以做什么？**  
> 主题：基于图像的自动化  
> 时间：少于30分钟  
> [点我下载示例文件][1]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/image-based-automation/introduction/
[1]: https://www.ranorex.com/rx-media/rx-user-guide/v8.2/download/RxSampleImageBased.zip  

## 安装

1. 将项目目录解压缩到计算机上的任何文件夹  
2. 启动Ranorex Studio并打开解决方案文件 `ImagebasedAutomation.rxsln`  

> **提示**  
> 示例解决方案适用于Ranorex 8.0或更高版本。您需要同意8.2及更高版本的自动解决方案升级。  

## 打开/关闭基于图像的自动化  

在录制期间的任何时候，都可以在Recorder控制中心打开和关闭基于图像的自动化。  

![B7010-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Image-basedAutomation/B7010-0000010.png)  
*打开/关闭基于图像的自动化*  

1. Ranorex Recorder中基于图像的复选框（未选中，即关闭）  
2. 基于图像的自动化已打开  

![B7010-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Image-basedAutomation/B7010-0000020.png)  
*通过Recorder热键激活基于图像的自动化*  

3. 在激活的记录器热键中按 `I` 键  
4. 基于图像的自动化已打开  

## 为什么基于图像的自动化？  

在GUI软件的自动测试中使用基于图像的自动化的原因可能并不明显。本节将向您展示基于文本的自动化失败的至少一个原因，并且基于图像的自动化是解决方案。 

### 实例准备  

使用Ranorex演示应用程序观察基于图像的自动化的演示示例。在此示例中，我们使用Ranorex Recorder的即时录制功能。 

![B7010-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Image-basedAutomation/B7010-0000030.png)  
*基于图像的自动化示例*  

1. 启动演示应用程序并选择**基于图像的自动化**作为工作环境  
2. 在Ranorex Studio Recorder的技术选择期间选择**即时录制**  

### 基于文本的录制  

在默认的基于文本的自动化模式下，在演示应用程序的日历视图中跟踪和记录三（3）个连续日期，并查看结果。  

![B7010-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Image-basedAutomation/B7010-0000040.png)  
*在基于文本的自动化中跟踪和记录日历日期*  

3. 验证是否已打开默认的基于文本的自动化（即未选择基于图像的自动化）  
4. 记录（点击）日历的“24”，“25”和“26”三个日期会导致...
5. 一个动作表，其中包含三个表示日历鼠标单击的相应操作项






