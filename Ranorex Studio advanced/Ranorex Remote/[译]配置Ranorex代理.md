# [译] 配置 Ranorex 代理

*原文地址 👉 [Configure Ranorex Agent][0]*  

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*  
*♋ translate time : 2018-6-26*    
*♋ update time : 2018-7-6*

---

打开Ranorex代理的主菜单的窗口如下图所示：

![B8040-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRemote/B8040-0000010.png)  

在代理窗口的右上角，打开主菜单:

- 更改显示名称
代理的显示名显示在代理窗口的左上角，在Ranorex Studio的远程面板中。如果您更改了代理的显示名，那么所有在代理列表中有此代理的人都必须从列表中删除具有前显示名的代理，并手动重新添加新的显示名。
- 更改许可证管理器
选择切换到另一个许可证管理器。
- 显示文件…
打开文件系统中的文件夹，该文件夹包含与代理相关的所有数据。
- 自动启动在登录
选择在登录到机器后自动启动Ranorex代理。
- 保持会话活动
此设置确保即使关闭远程会话，用户会话也保持解锁。

有关更多信息，请参阅⇢[远程常见问题][1]部分。

> **注意：**  
> - 由于这种机制会使您的远程机器解锁，即使您断开了RDP会话，现在也禁用了基本的安全机制。请注意，由于系统安全性被禁用，您的远程机器现在可以轻松访问。 我们建议您不要在远程机器上存储敏感数据。  
> - 当结束活动的RDP会话并切换到未锁定的远程会话时，远程计算机可能会更改为其他屏幕分辨率。如果您的远程计算机是虚拟机，则可能会发生这种情况。 在这种情况下，可能会使用虚拟机的默认屏幕分辨率。 这可能会影响您的测试。

- 总在最前面
选中此选项可在所有其他窗口上显示代理的窗口。
- 退出
选择关闭代理并释放许可证。在Ranorex Studio的远程面板中，此代理将显示为无法访问。

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorex-remote/configure-ranorex-agent/
[1]: .\[译]远程常见问题.html


