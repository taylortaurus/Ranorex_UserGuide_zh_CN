# [译] 管理控件库项目

*原文地址 👉 [Manage repository items][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2019-9-9*    

---

一旦他们成为您的控件库的一部分，您就可以编辑和管理编辑和管理控件库项目的多种方法。本章介绍了可用的选项。

**本章导视**


- [重命名控件库项目](#重命名控件库项目)
- [复制/移动/删除控件库项目](#复制/移动/删除控件库项目)
- [更新截图](#更新截图)
- [突出显示元素](#突出显示元素)
- [添加验证截图](#添加验证截图)
- [查找指引](#查找指引)
- [控件库项属性](#控件库项属性)
  
  ## 重命名控件库项目

Ranorex Studio根据在跟踪的应用程序中调用相应的UI元素自动分配控件库项目名称。有时，这些名称可能含糊不清或过于通用，导致难以浏览控件库。您可以重命名控件库项目，以使其更清晰。

![A7040-0000011](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7040-0000011.png)         
*重命名控件库项目*
1. 选择控件库项目，然后按 F2。

2. 重命名控件库项目，然后按Enter键。

3. 控件库项的名称已更改。


## 复制/移动/删除控件库项目

可以像往常一样复制，移动和删除控件库项目。但是，移动和删除可能会导致以下问题：

- 您将控件库项移动到控件库中的逻辑边界。
- 您删除链接到一个或多个动作的控件库项目。


### **跨越逻辑边界**
Ranorex将控件库项目组织在称为文件夹的逻辑组中。文件夹始终包含对UI元素的引用，这些元素在UI中共享相同的基本位置。这个概念在章节⇢[构建控件库项目][2]中有详细解释。

将控件库项目从一个文件夹移动到具有不同基本路径的文件夹时，还会更改存储库项目的基本路径。因此，Ranorex可能无法再找到UI元素，并且在测试执行期间链接到此存控件库项的任何操作都将失败。当您尝试以这种方式移动项目时，Ranorex会要求您确认。

![A7040-0000021](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7040-0000021.png)      
*跨逻辑边界移动控件库项目*

1. 当您使用不同的基本路径将控件库项目从一个文件夹移动到另一个文件夹时...

2. ... Ranorex将通知您有关后果并要求您进行确认。

 
>**贴士**        
这仅适用于app folder和root folder。simple fold不受影响，因为它们没有基本路径。


## 删除链接的控件库项目
删除链接到一个或多个动作的控件库项时，动作将停止工作。如果要删除未使用的控件库项，请改用清除功能

![A7040-0000031](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7040-0000031.png)       
*删除控件库项目*

1. 选择控件库项并将其删除。

2. 控件库项目将从链接到的动作中删除。这些行动将不再有效。


## 更新截图
创建控件库项时，还会保存相应UI元素的屏幕截图。它可以在控件库中查看。当UI元素在外观上发生变化时，您可能需要更新它。选项更新屏幕截图允许您快速执行此操作，而无需回溯UI元素。

![A7040-0000041](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7040-0000041.png)       
*更新控件库项屏幕截图*
1. 更新截图选项
- 右键单击要更新其屏幕截图的控件库项
- 单击`update screenshot`
2. 截图

3.失败弹窗

- 只有在UI元素的路径仍然有效且包含的应用程序正在运行且UI元素可见时，才能更新屏幕截图。如果不是这种情况，则会显示错误失败弹窗。


## 突出显示元素
有时，很难确定控件库项目引用的UI元素。单击“Highlight element”时，Ranorex Studio将突出显示包含应用程序中的UI元素。当然，这只有在Ranorex Studio可以找到元素时才会起作用，即如果包含的应用程序正在运行并且元素的路径是正确的。

![A7040-0000051](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7040-0000051.png)      
*突出显示控件库项目*

1. 突出显示元素
- 右键单击所需的存储库项。
- 单击Highlight element。
2. 该UI元素被高亮显示在应用了几秒钟以闪烁的红色帧。 

![A7040-0000061](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7040-0000061.png)       
*搜索相应的UI元素*

1. 搜索相应的UI元素
- 有时Ranorex可能需要一段时间才能找到相应的UI元素。
- 如果路径不正确或尚未启动包含的应用程序，Ranorex将无法找到该元素。

## 添加验证截图
此选项对⇢[图像验证][3]很有用。通常，当您记录图像验证时，将自动创建验证屏幕截图。但是，您也可以手动添加验证屏幕截图。您还可以将多个验证屏幕截图添加到单个控件库项目中。在对不同状态下的相同UI元素进行图像验证时（例如，交通信号灯状态字段），这非常有用。选项添加验证屏幕截图可让您执行此动作。   

![A7040-0000071](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7040-0000071.png)        
*创建验证屏幕截图*

1. 右键单击所需的控件库项。

2. 单击Add validation screenshot

3. UI元素的当前状态的屏幕截图将添加到相应的控件库项目中。

>**贴士**          
此选项仅在打开AUT并且相应的UI元素可见时才有效。


### **保存截图**
将验证屏幕截图添加到控件库项目后，您可以将其保存到系统上的任何目标位置。然后，您可以使用⇢[图像编辑器][4]恢复保存的屏幕截图。

![A7040-0000081](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7040-0000081.png)        
*保存控件库截图*

1. 右键单击屏幕截图，然后单击Save screenshot...


## 查找引用
在大型测试项目中，可以在许多模块和/或代码段中引用存储库项。这就是为什么在对其进行更改之前检查控件库项目的确切位置是有意义的。两个上下文菜单选项查找测试模块引用和查找代码引用允许您这样做。

### **查找测试模块参考**
此选项显示引用控件库项的所有测试模块。

![A7040-0000091](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7040-0000091.png)

1. 右键单击所需的存储库项。

2. 单击查找测试模块引用。

3. 引用显示在Ranorex Studio底部的搜索结果中。


### **查找代码引用**
此选项显示引用控件库项的所有代码实例。

![A7040-0000101](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7040-0000101.png)

1. 右键单击所需的控件库项。

2. 单击“Find code references”，然后选择两个选项之一。

3. 代码引用显示在Ranorex Studio底部的搜索结果中。


## 控件库项属性
每个控件库项目还具有一组可在其“属性”面板中配置的属性。
![A7040-0000111](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7040-0000111.png)       
*打开控件库项属性*

1. 右键单击所需的控件库项。

2. 单击Properties。

3. 属性在控件库右侧打开。


### **属性列表**
Absolute Path（绝对路径）	         
表示控件库项的路径，包括所有父文件夹的路径。只读。

Adapter type （适配器类型）                          
允许您选择适配器类型。默认情况下，Ranorex会自动选择最合适的适配器。
                    
Effective timeout（超时有效期）            
应用于特定控件库项及其所有父文件夹的所有搜索超时的总和。只读。


Comment（备注）        
允许您向控件库项添加注释。
          
Live element（活动元素）              
当控件库项目表示的UI元素处于活动状态时，即打开AUT并且元素可见时，此属性会为其显示一系列不同的参数。

Name   （名称）                  
控件库项的名称。

Search timeout（搜索超时时间）           
定义Ranorex在抛出异常之前搜索元素的时间量。

Use ensure visible  （使用确保可见）                   
当被设置为Yes的时候，强制使控件库项表示的UI元素在测试运行期间变为可见。例如，UI元素可能位于网页的底部，您需要先滚动到该网页才能看到它。启用此属性后，Ranorex将自动执行此操作。
设置为“默认”时，该属性将从“常规”设置中默认使用“确保可见”设置继承。

Use cache （使用缓存）              
仅适用于app folder和rooted folder。
当这是True时，Ranorex会在找到文件夹时缓存文件夹所代表的UI元素。这可以加快自动化速度，因为Ranorex将不再搜索元素的路径。但是，如果UI元素定期更改，我们建议您将其设置为False。在这些情况下，缓存会降低测试运行速度并在报告中生成警告消息。这是因为缓存的元素与实际元素不匹配，Ranorex将使用绝对路径搜索它。这也适用于返回两个或更多UI元素的文件夹。Ranorex将始终缓存它找到的第一个UI元素，然后使用绝对路径再次搜索其余元素，从而导致速度减慢。
手动创建的文件夹的默认值：
App folder：False
Rooted folder：False
自动创建的文件夹的默认值是根据UI元素的技术设置的。在大多数情况下，这意味着错误。




---

[👈创建控件库项][1]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[构建控件库项👉][2]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/repository/managing-repository-items/
[1]:.\creation-repository-items.html
[2]:.\structuring-repository-items.html
[3]:.\test-validation\image-based-validation-example.html
[4]:.\ranorex-studio-advanced\image-based-automation\introduction.html