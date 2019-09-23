# [译] 管理动作


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月6日-green.svg?longCache=true&style=flat-square)


---

在本章中，您将学习手动添加动作，配置动作和管理动作。

**本章导视**
- [添加新动作](#添加新动作)
- [配置动作](#配置动作)
- [动作组件](#动作组件)
- [上下文菜单设置](#上下文菜单设置)
- [属性](#属性)
  
  
>**视频向导**   
>视频“管理动作”将引导您完成本章中的内容。   
[立即观看](https://www.youtube.com/embed/mpWYmh89dlU)

## 添加新动作
录制期间会自动生成许多动作。但是，必须手动添加某些动作。手动添加动作有两种方法：使用菜单选项或将控件库项拖放到动作表。

### **从菜单添加动作**

![A6040-0000011](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6040-0000011.png)     
*添加新动作 - 菜单*

1. 在动作表工具栏中添加新的动作菜单。
2. 在动作表上下文菜单中添加新的动作菜单选项。

将控件库项拖放到actions表

![A6040-0000021](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6040-0000021.png)

1. 选择一个库项目，并移动至在动作表。

2. 这将打开上下文菜单，其中包含此控件库项的所有可能动作，`单击`所需的动作。

>**注意**    
新动作将自动链接到控件库项目。

### **配置动作**
动作表是您配置动作的位置。您可以通过动作的组件、上下文菜单及其属性（其中一些重叠）输入不同的设置。

### **行动组件**
动作表包含七个不同的列。这些列表示动作的五个不同组件。某些动作组件较少，其他组件更多。组件分组如下：

![A6040-0000031](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6040-0000031.png)      
*行动组件*


1. 动作符号和序列号

- 每个动作都有自己的符号。
- 序列号告诉您执行动作的顺序。

2. 动作类型

- 动作类型指示动作执行的动作或动作的UI设备的哪个部分。

3. 动作细节

- 列3-5的内容根据动作类型而变化。
- 它们详细定义了动作的作用：例如，键序列的确切文本字符串或鼠标单击的类型。
  
4. 控件库项目

- 执行动作的控件库项目，即动作的目标。
- 控件库项表示AUT中的UI元素。
- 控件库项目与动作分开管理，但它们彼此链接。

>**章节预览**
> Ranorex Studio基础>👉[控件库][1]中引入了控件库和控件库项。

1. 备注
 - 您可以在此处添加注释以记录动作的作用。这对动作本身没有影响。

### **动作截图**
当您使用Ranorex Recorder录制针对UI元素的动作时，将保存动作的屏幕截图。您可以在动作表旁边查看此屏幕截图。单击屏幕截图以查看或隐藏它。

![A6040-0000041](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6040-0000041.png)     
*打开/关闭屏幕截图*

### **上下文菜单设置**
动作的上下文菜单可让您快速访问多个设置，其中一些设置仅适用于某些动作。您还可以一次选择多个动作以将上下文菜单设置应用于它们。选择多个动作时，可以使用不同的设置。

![A6040-0000051](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6040-0000051.png)     
*上下文菜单包含所有可用选项*

>**贴士**   
>前四项称为运行选项。它们在Ranorex Studio基础> Ranorex 录制器>[👉运行和调试录制][2]中进行了解释。

### **单动作设置**
Highlight element：突出显示AUT中的链接控件库项。AUT必须正在运行。仅适用于链接到控件库项目的动作。

Add new action：在当前动作后添加新动作。

Make repository item variable…：使链接的控件库项成为变量。仅适用于链接到控件库项目的动作。

Set search timeout…：定义Ranorex在动作失败之前尝试查找链接控件库项的时间。仅适用于链接到控件库项目的动作。

Enable/Disable continue on fail：设置Ranorex是否将进入下一个动作，或者如果此测试失败，则中止测试。默认设置已禁用。如果启用此选项，受影响的动作将在动作表中以斜体显示。

Enable/Disable：设置在测试执行期间是运行还是跳过动作。默认设置已启用。已禁用的动作在动作表中显示为灰色。

View code：在代码编辑器中显示动作的基础代码。对专家配置和👉[用户代码动作][3]很有用。

Convert to user code：将动作转换为👉[用户代码动作][3]。

Move to new recording module：创建包含所选动作的新录制模块。

Cut/Copy/Paste/Delete：剪切，复制，粘贴或删除所选动作。

Properties：打开动作的属性，本章稍后将对此进行说明。

### **多动作设置**

![A6040-0000061](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6040-0000061.png)     
*多动作设置的上下文菜单*

将项目合并到用户代码项：将动作代码合并为单个👉[用户代码动作][3]。用于组合高级方案的多个动作。

合并选定的键盘项：当两个或多个键序列动作或键快捷键动作链接到同一控件库项时，您可以将键按下组合为单个动作以合并它们，这对于组合无意中分成几个动作的键盘输入很有用。

## 属性
动作属性是用于控制动作的各种选项。有两组动作属性：标准属性和特定于动作的属性。标准属性定义适用于大多数动作类型的动作，如下所述。特定于动作的属性定义仅适用于特定动作类型的动作。

>**贴士**    
在Ranorex Studio基础>动作> 👉[动作属性][4]中描述了特定于动作的属性及其相关动作。

有两种方法可以访问动作的属性：

a.右键单击某个动作，然后单击“Properties”。

b.单击一个动作，然后按 F4。

这些也适用于多个动作。然后，属性面板将显示所选动作之间共享的所有属性。

![A6040-0000071](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6040-0000071.png)     
*访问动作属性的一种方法*
 
### **标准属性**
在这里，您可以找到所有标准属性的列表以及有关它们的详细信息。可以为几乎所有动作类型配置它们。默认值以粗体显示。

![A6040-0000081](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6040-0000081.png)     
*标准动作属性*

1. 备注

- 可能的值：空或文本。
- 添加备注。也可以直接在动作表中设置。
- 适用于除分隔符动作之外的所有动作


2. 失败后继续

- 可能的值：false或true
- 如果设置为false，则此动作失败时测试执行将停止。
- 如果设置为true，则当此动作失败时，测试执行将继续执行下一个动作。


3. 持续时间

- 可能的值：以毫秒为单位的时间（默认值因动作而异）
- 定义的动作持续时间
- 适用于除报告和分隔符动作之外的所有动作

4. 启用

可能的值：true或false
启用或禁用动作。您也可以选择一个动作，然后按  Ctrl  +  E 启用或禁用它。

5. 控件库项目

可能的值：对控件库项的引用
动作链接到的控件库项。
适用于可以链接到控件库项目的所有动作。

6. 使用日志记录

可能的值：Default，true或false
设置是否将动作记录到报告中。
设置为“默认”时，此值将从“使用”项目记录中继承默认设置👉[记录默认][5]，它是默认启用的。因此，默认情况下会记录所有动作。
可用于除Separator动作之外的所有动作，该动作始终记录。

---
[👈动作和控件库项][6]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[动作属性👉][4]


[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/actions/managing-actions
[1]:.\repository\Introduction.html
[2]:.\ranorex-recorder\run-debug-recordings.html
[3]:.\user-code-actions.html
[4]:.\action-properties.html
[5]:.\ranorex-studio-system-details\settings-configuration\[译]Ranorex录制器设置.html
[6]:.\actions-repository-items.html