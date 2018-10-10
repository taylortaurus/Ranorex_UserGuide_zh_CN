# [译] Ranorex 代理

*原文地址 👉 [Ranorex Agent][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-6-26*  
*♋ update time : 2018-7-6*  

---

Ranorex Agent是一个独立的工具，支持远程测试执行。

要闻速览：

- Ranorex代理对多个请求进行排队，每次⇢[执行][1]一个测试。
- Ranorex代理可以⇢[安装][2]在物理机和虚拟机上。
- 每台机器可以安装一个Ranorex代理。
- 运行Ranorex代理需要一个活动用户会话。
- 远程执行的测试功能齐全，包括鼠标和键盘操作。
- Ranorex运行时许可证是远程测试执行所必需的。 启动代理程序时，它会自动从安装在网络中的许可证管理器请求。一旦代理关闭，许可将被释放。

当Ranorex Agent启动时，Windows系统托盘中将显示一个图标。 要打开Ranorex Agent窗口，只需点击此图标：

![B8020-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRemote/B8020-0000010.png)  

使用此图标的上下文菜单，你可以打开和关闭代理的窗口。选择“退出”关闭代理。关闭代理将释放许可证，关闭整个应用程序。在此操作之后，远程运行测试是不可能的。  

![B8020-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRemote/B8020-0000020.png)  

Ranorex代理的窗口显示代理的作业队列以及代理的日志(包括技术细节)和代理的显示名。机器的主机名显示在标题栏中。

![B8020-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRemote/B8020-0000030.png)  

你还可以配置代理的设置。 有关此主题的更多信息，请访问此部分：⇢[配置Ranorex代理][3]  

作业队列提供了当前执行和计划测试的概述。这些作业是通过它们各自的测试套件名称列出的，并且颁发者会看到正在运行Ranorex Studio的机器名称。

![B8020-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRemote/B8020-0000040.png)

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorex-remote/ranorex-agent/
[1]: .\[译]执行测试.html
[2]: .\[译]Ranorex代理的安装和设置.html
[3]: .\[译]配置Ranorex代理.html