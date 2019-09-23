# [译] 调用动作

*原文地址 👉 [Invoke Actions][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2019-9-9*    

---
Invoke动作允许您对控件库项执行动作，而无需任何直接交互，如鼠标单击或键盘输入。这对于动作不可见的 UI元素特别有用，例如失焦的窗口或需要滚动的列表项。在本章中，您将通过两个示例学习如何使用Invoke动作。

**本章导视**

- [单击简单按钮](#单击简单按钮)
- [列出项目选择](#列出项目选择)

>**视频向导**   
视频“调用动作”将引导您完成本章中的内容。  
[立即观看](https://www.youtube.com/embed/uqGwdcJj9Go)


## 单击简单按钮
在此示例中，您将使用Invoke动作执行简单的按钮单击。下图中的动作＃1在AUT 的添加条目按钮上执行鼠标单击。

![A6060-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6060-0000010.png)      
*鼠标单击添加条目按钮上的动作*     

要使用执行相同动作的Invoke动作替换它：
1. 单击`Add new action`> `Invoke action`。

2. 动作表中将显示空的Invoke动作。

![A6060-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6060-0000020.png)      
*添加Invoke动作*

3. 从控件库中，将表示添加条目按钮的项目BtnAddPerson 拖到 Invoke动作。

![A6060-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6060-0000030.png)         
*将存控件项链接到Invoke动作*

4. 在Invoke动作的Action name列中，选择 `PerformClick（）`。

![A6060-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6060-0000040.png)         
*指定调用动作类型*

5. 最后，右键单击常规鼠标单击动作，然后单击`disable`以禁用它。

### **结果：**
现在可以直接执行单击`Add Entry`按钮而无需任何鼠标交互。

## 列出项目选择
自动列表项选择可能具有挑战性，因为通常，某些项目不会立即可见。使用Invoke动作而不是常规鼠标交互通常可以使您的测试更加稳健。下图显示了使用鼠标单击动作选择的标准列表项。

![A6060-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6060-0000050.png)      
*列出项目选择*

1.鼠标单击动作，打开`Department`下拉列表。

2.鼠标单击从列表项中选择`Project Management`的动作。

要使用Invoke动作执行此动作：
1. 单击`Add action`> `Invoke action`两次以添加两个空Invoke动作。

2. 从系统信息库，拖动该项目打开代表的下拉按钮，第一Invoke动作。 使用表示Project Management列表项的ProjectManagement项重复第二次Invoke动作。

3. 在第一个Invoke动作的Action name列中，选择`Press（）`。使用`Select（）`重复第二次Invoke动作。
最后，右键单击常规鼠标单击动作，然后单击`disable`以禁用它们。

![A6060-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6060-0000060.png)        
*调用列表项选择的动作*

### **结果**：
- 现在直接执行列表项选择，无需任何鼠标交互。

---
[👈动作属性][1]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[用户代码动作👉][2]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/actions/invoking-actions/
[1]:.\action-properties.html
[2]:.\user-code-actions.html
