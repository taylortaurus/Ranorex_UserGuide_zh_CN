# [译] 使用单个控件库项表示多个元素

*原文地址 👉 [Represent multiple elements with a single repository item][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2019-9-10*    

---

有时，单个控件库项表示多个UI元素可能会有所帮助。示例包括单选按钮和复选框等元素。此功能通常与代码模块一起使用。

**本章导视**
- [必要的背景](#必要的背景)
- [示例定义](#示例定义)
- [跟踪控件库项目](#跟踪控件库项目)
- [概括RanoreXPath规范](#概括RanoreXPath规范)
- [多个控件库项检测](#多个控件库项检测)
- [将跟踪的项添加到控件库](#将跟踪的项添加到控件库)
- [命名通用控件库项](#命名通用控件库项)




>**视频向导**        
视频“使用单个控件库项表示多个元素”将引导您完成本章中的信息：           
[立即观看](https://www.youtube.com/embed/_vRlv6shus4)

## 必要的背景
本章介绍的概念通常与代码模块一起使用，代码模块是一个专家级别的主题。此外，如果您熟悉RanoreXPath语法和Ranorex Spy工具，您会发现该示例更容易理解。使用以下链接了解有关这些高级主题的更多信息。

>**章节预览**              
代码模块在> Ranorex Studio专家> 👉[代码模块][1]中引入。            
RanoreXPath语法在> Ranorex Studio高级>  👉[RanoreXPath][2]中描述。              
在> Ranorex Studio高级> 👉[RanorexSpy][3]中了解Ranorex Spy工具  。

## 示例定义
在以下示例中，一个控件库项表示两个单选按钮。这些单选按钮显示在演示应用程序中数据库的性别选择区域内。

![A7080-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7080-0000010.png)              
*演示应用程序中的性别选择按钮*


## 跟踪控件库项目
创建表示多个元素的控件库项的过程与常规控件库项的过程相同。请参阅以下说明：

1. 打开Ranorex间谍 

2. 开始的演示应用程序  ，并单击测试数据库中注册标签

3. 跟踪的性别选择一个单选按钮

![A7080-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7080-0000020.png)                 
*跟踪演示应用程序中的单选按钮*

1. 在演示应用程序中跟踪和识别女性单选按钮的UI元素
2. 在Ranorex Spy中女性单选按钮的唯一Ranorexpath规范
3. 在Ranorex Spy中UI元素浏览器树显示了定义过的女性单选按钮路径
4. 在Ranorex Spy中女性单选按钮的路径编辑器



## 概括RanoreXPath规范
按照以下步骤概括RanoreXPath规范，使其包含演示应用程序的第二个性别选择单选按钮。

1. 更改RanoreXPath规范，如下所示

![A7080-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7080-0000030.png)            
*RanoreXPath规范的推广*

1.初始RanoreXPath规范，仅包括女性单选按钮 

2.修改后，包含两个单选按钮的通用RanoreXPath规范

## 多个控件库项检测
推广RanoreXPath规范可以同时跟踪演示应用程序中的性别选择单选按钮。这可以在Ranorex Spy中看到。

![A7080-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7080-0000040.png)                  
*多个控件库项跟踪*

3.匹配到的两个被跟踪的单选按钮

![A7080-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7080-0000050.png)                  
*在Ranorex Spy中找到元素信息*

4.Ranorex Spy在工作环境的左下角显示匹配结果

## 将跟踪的项添加到控件库
最后，将匹配的项添加到控件库。

![A7080-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7080-0000060.png)         
*将匹配的项添加到控件库*

1. 选择一个匹配的控件库项，打开上下文菜单，然后单击“Add to repository”


## 命名通用控件库项
与所有控件库项一样，可以重命名通用控件库项以使其更有意义。

![A7080-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7080-0000070.png)           
*命名通用控件库项*


1. 选择表示多个UI元素的控件库项。

2. 打开上下文菜单以更改控件库项目名称。


---
[👈清理控件库][4]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[管理多个控件库👉][5]

[0]:https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/repository/repository-items-representing-multiple-elements/
[1]:.\ranorex-studio-expert\code-modules\introduction.html
[2]:.\ranorex-studio-advanced\ranorexpath\introduction.html
[3]:.\ranorex-studio-advanced\ranorex-spy.html
[4]:.\repository-cleanup.html
[5]:.\Manage-multiple-repositories.html