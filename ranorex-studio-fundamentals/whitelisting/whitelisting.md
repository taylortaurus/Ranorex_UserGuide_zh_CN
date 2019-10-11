# [译] 白名单

*原文地址 👉 [Whitelisting][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2019-9-10*    

---

在识别UI元素时，Ranorex Studio及其组件默认扫描计算机上的所有正在运行的进程。通过白名单，您可以将Ranorex Studio专注于与测试相关的流程。

这有两个好处：

- 它可以在测试录制，测试执行和Ranorex Spy中提高性能
- 它可以帮助您创建干净的录制，因为您只能与白名单进程进行交互。


>**贴士**            
提前计划哪些流程将成为您测试的一部分，并将其添加到白名单中。

## 编辑白名单
1. 在Ranorex工作室，View>whitelist。白名单打开。

2. 如果白名单为空，请单击编辑白名单...或单击打击垫右上角的白名单图标。

3. 出现编辑窗口。在里面：

a. 将进程添加到白名单或使用按钮删除它们。

b. 如果左侧未列出进程，请单击“Add process...”以浏览到该进程并直接添加。

c. 单击“Advanced...”以打开一个对话框，您可以在其中粘贴进程名称列表或使用正则表达式语句指定一系列进程名称。

![A8100-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/whitelisting/A8100-0000010.png)


4. 完成后，单击“Apply whitelist”。Ranorex Studio及其组件现在只能在白名单进程中识别UI元素。

>**贴士**                 
端点不受白名单的影响，因此仍会出现在Spy中。

>**章节预览**          
了解有关端点的更多信息
Web和移动测试>端点> ⇢[入门][1]

### **结果**  

![A8100-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/test-validation/A8100-0000020.png)

1. 没有白名单的Ranorex Spy浏览器窗口

2. 具有活动白名单的Ranorex Spy浏览器窗口和白名单中的Ranorex Studio演示应用程序


---

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/whitelisting/

[1]:.\web-mobile-testing\Endpoints\getting-started.html

