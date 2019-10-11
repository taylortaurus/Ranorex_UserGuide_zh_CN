# [译] 动作和报告

*原文地址 👉 [Actions and the report][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2019-9-10*     

---

在本章中，您将了解在测试运行期间执行的动作如何在报告中表示。


**本章导视**

- [如何报告动作](#如何报告动作)
- [报告中的动作是什么样的](#报告中的动作是什么样的)



>**视频向导**          
视频“动作和报告”将引导您完成本章中的信息。         
[立即观看](https://www.youtube.com/embed/xglCJQNoCgk)

## 如何报告动作
默认情况下，测试运行期间执行的每个动作都会触发报告消息。

![A9020-0000011](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9020-0000011.png)

1. 测试运行期间报告的动作
如上图所示，一个动作意味着至少一条报告消息，有时甚至更多。在具有数千个动作的大型测试套件中，报告可能会非常快速地混乱。为了防止这种情况，您可以使用👉[报告等级][6]以控制哪些报告消息进入报告。
您还可以通过其属性完全禁用动作报告。

>**章节预览**            
禁用报告动作的解释如下：            
> Ranorex Studio基础>动作> 👉[管理动作][1]

## 报告中的动作是什么样的
根据报告在报告中的显示方式，动作可分为四组：

- 验证失败或成功
- 分隔符
- 用户定义的日志消息
- 所有其他动作


### **验证**
验证报告消息总是包含两部分。第一部分具有报告级别信息，并且只是已执行验证的通知。

第二个部分告诉您验证是成功还是失败。

![A9020-0000021](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9020-0000021.png)

1. 成功验证                  
成功验证的报告级别为Success，默认情况下以绿色打印。

2. 验证失败                     
失败的验证具有报告级别失败，具有红色背景，并且通常附带两个屏幕截图，以便更容易找出出错的地方。

>**章节预览**                    
要了解有关验证的更多信息，请参阅以下章节：                       
Ranorex Studio基础>动作>  👉[动作属性][2]            
和                
Ranorex Studio基础> 👉[测试验证][3]

### **分隔符**
分隔符对于在action表和报告中直观地构造动作非常有用。

![A9020-0000031](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9020-0000031.png)

1. 动作表中的分隔符，接下来是标题验证动作。
2. 在报告中，分隔符具有报告级别Info，其消息显示在actions表中定义的标题。
 
>**章节预览**                 
有关分隔符的更多信息，请参阅            
Ranorex Studio基础知识> Ranorex Recorder>  👉[管理录制模块][4]
和                       
Ranorex Studio基础>动作>  👉[动作属性][2]

用户定义的日志消息
使用“log”消息动作，您可以将具有自定义报告级别的自定义消息传递给报告。


![A9020-0000041](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9020-0000041.png)


1. 在动作表中记录消息。
2. 报告中的相同日志消息。

>**章节预览**      
有关日志消息动作的更多信息，请参阅            
Ranorex Studio基础>动作>  👉[动作属性][2]

### **所有其他动作**
所有其他动作都具有报告级别信息，其消息描述了他们正在执行的动作。如果此类动作失败，则报告级别失败的单独消息将以与上面进一步描述的验证相同的方式传递给报告。

![A9020-0000051](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9020-0000051.png)


1. 鼠标单击动作具有报告级别信息，其文本描述了在指定的屏幕坐标处对指定的控件库项目执行了左键单击。


---

[👈简介][5]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[报告等级👉][6]


[0]:https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/reporting/basic-report-characteristics-data/

[1]:.\actions\managing-actions.html
[2]:.\action-properties.html
[3]:.\test-validation\.introduction.html
[4]:.\ranorex-recorder\managing-recording-modules.html
[5]:.\introduction.html
[6]:.\concept-report-levels-2.html