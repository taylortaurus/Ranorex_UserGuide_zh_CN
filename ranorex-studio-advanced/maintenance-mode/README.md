# [译] 维护模式

*原文地址 👉 [Maintenance mode][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-14*    

---

维护模式允许你在测试执行期间捕获并解决某些错误。然后，你可以从报告中将修复程序应用于测试套件。这样可以节省时间，因为你不必让整个测试运行来开始诊断和修复错误。

本章导视，章节内段落跳转推荐使用右上角的锚点！

- [激活维护模式](#激活维护模式)
- [捕捉和解决错误](#捕捉和解决错误)
- [应用修复](#应用修复)  

## 激活维护模式

1. 确保调试时启用下  构建>设置配置。该选项通常默认启用。它与你从菜单栏启用的调试模式不同。

    ![B9000-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/MaintenanceMode/B9000-0000010.png)  

2. 使用测试套件视图中的开关激活维护模式。现在，当你运行测试时，它将以维护模式执行。关闭测试套件视图并重新打开时，将再次关闭维护模式。

    ![B9000-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/MaintenanceMode/B9000-0000020.png)

**注意**
> 在Ranorex代理上无法使用维护模式运行测试。

## 捕捉和解决错误  

当维护模式处于活动状态时，它会捕获ranorex本机错误，并在执行时暂停测试执行。根据错误类型的不同，将出现具有不同选项的不同对话框。

下述选项可供选择

|选项|说明|
|:--|:--|
|Open report|打开报告|
|Continue with error|根据测试容器的设置⇢[错误行为][1]，将继续执行测试|
|Abort test run|终止测试|

### 元素未找到  

无法找到存储库元素时，将显示此对话框。它显示相关的错误消息和元素的RanoreXPath。

单击编辑，然后重新打开Ranorex Spy。你可以手动回放元素或更改其路径。在Spy中应用更改后，Ranorex Studio将自动尝试使用更新的路径再次运行失败的操作。

你也可以单击`Retry`重试，而不进行任何更改。如果你认为路径正确并且由于搜索超时太短或SUT尚未达到正确状态而无法找到该元素，这将非常有用。

![B9000-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/MaintenanceMode/B9000-0000030.png)  

### 验证失败

无法验证值时，将显示此对话框。它显示带有预期值和实际值的验证错误消息。

下拉菜单包含预期值（第一个选项）和实际值（第二个选项）。选择实际值，然后单击“ 应用”并重试以使用此值再次运行失败的操作。


**注意**  
> 在维护模式下无法解析图像验证，将显示通用对话框。

![B9000-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/MaintenanceMode/B9000-0000040.png)  

### 通用对话框  

此对话框显示当前在维护模式下无法解析的所有Ranorex本机错误。单击`Open Spy`以检查Ranorex Spy中受影响的元素，这可以帮助你诊断错误发生的原因。

![B9000-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/MaintenanceMode/B9000-0000050.png)  

## 应用修复

一旦解决了维护模式中出现的错误并且测试已成功执行，你就可以在报告中将修复程序应用于测试套件。

在报告中，维护模式事件由特殊图标指示：

![B9000-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/MaintenanceMode/B9000-0000060.png)  

展开报告项以接收更多信息。使用绿色复选标记查找维护模式事件并将鼠标悬停在其上以将修复程序应用于测试套件：

![B9000-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/MaintenanceMode/B9000-0000070.png)  


**注意**  
> 无法自动应用变量和数据绑定的修复。你需要手动修复这些问题。以上适用于验证值和RanoreXPaths。


[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/maintenance-mode/
[1]: ..\\..\\..\\ranorex-studio-fundamentals/Test_suite/[译]执行测试套件.html