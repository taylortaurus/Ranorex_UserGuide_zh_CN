# [译] 远程常见问题

*原文地址 👉 [Remote FAQ][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*  
*♋ translate time : 2018-7-5*  
*♋ update time : 2018-7-6*

---

这些有关Ranorex Remote的常见问题是想要帮助你快速找到重要主题的答案。只需点击其中一个问题即可获得答案。

## 我可以在虚拟机上安装Ranorex代理吗？
----

是的，Ranorex代理可以安装在虚拟机和物理机上。

## 我可以在同一台机器上安装多个Ranorex代理吗？
---

一个Ranorex代理可以安装在一个操作系统中。
如果要在物理计算机上运行多个Ranorex代理，则必须在该计算机上设置更多操作系统。

## Ranorex Remote需要哪种类型的许可证？
---

Ranorex代理使用通过Ranorex许可证管理器提供的一个Ranorex运行时许可证。

## 在Ranorex代理上执行远程测试需要多少许可证？
---

Ranorex代理在启动时获取Ranorex运行时许可证，并在代理关闭之前保留它。相同的许可证用于测试执行。Ranorex代理正在运行时，一个许可证被阻止 - 无论代理是空闲（没有执行测试）还是执行测试。 此外，代理执行的测试数量对使用的许可证数量没有影响。

## 如何将设置部署到Ranorex代理？
---

在本地计算机上配置的设置，例如：技术插件设置，可以使用Ranorex解决方案部署到远程计算机。请按照以下步骤操作：

- 打开Windows资源管理器并导航到本地计算机上的`%appdata%`。
- 复制文件'RanorexConfig6.xml'。
- 打开你的测试套件项目的文件系统目录。

![B8120-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRemote/B8120-0000010.png)    

- 在此文件夹中粘贴“RanorexConfig6.xml”。
- 切换回Ranorex Studio并启用在Projects View中显示所有文件。配置文件应该在列表中可见。  

![B8120-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRemote/B8120-0000020.png)  

- 在项目中包含配置文件。

![](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRemote/B8120-0000030.png)  

- 打开文件的“属性”窗格。使用上下文菜单或按F4执行此操作。
- 将属性“复制到输出目录”更改为“PreserveNewest”。

![](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRemote/B8120-0000040.png)  

使用此设置，配置文件将始终部署到Ranorex代理。

如果在此过程后更改任何设置，则必须手动更新此项目中的文件。 重复步骤1到4以执行此操作。

## 如果关闭远程会话，如何确保用户会话保持解锁状态？
---

Ranorex Remote需要一个活动的用户会话来在远程机器上运行测试。你可以使用远程桌面连接(RDP)连接到远程机器。只要这个远程连接是活动的，远程机器就被解锁，可以执行测试。如果断开RDP会话，你的远程机器将被锁定。由于在锁定模式下没有GUI可用，你的远程测试将失败。Ranorex 6.0.1及更高版本附带的Ranorex代理包括默认启用的“保持会话活动”设置。因此不需要更多操作，可在[配置 Ranorex 代理](.\[译]配置 Ranorex 代理.html)一章中找到更多信息。即使你已在Ranorex 6.0中断开RDP会话，也要保持远程会话未锁定，请按照以下说明操作：

- 在远程计算机上创建批处理文件并插入以下代码：

```bash
for /f "skip=1 tokens=3 usebackq" %%s in (
 `query user %username%`
) do (
 %windir%System32tscon.exe %%s /dest:console
)
```

- 将此批处理文件保存在远程计算机的桌面上并命名为：'KeepSessionOpen.bat'。
- 如果你需要断开RDP会话，现在只需使用管理员权限运行此批处理文件，你的远程计算机将保持解锁状态。

> **注意：**  
> - 由于即使你已断开RDP会话，此机制也会使你的远程计算机保持解锁状态，因此现在禁用了基本的安全机制。 请注意，现在可以在禁用系统安全性的情况下轻松访问远程计算机。 我们建议你不要在远程计算机上存储敏感数据。  
> - 当结束活动RDP会话并切换到未锁定的远程会话时，远程计算机可能会更改为不同的屏幕分辨率。 如果你的远程计算机是虚拟机，则可能会发生这种情况。 在这种情况下，可能会使用虚拟机的默认屏幕分辨率。 这可能会影响你的测试。

## 如何克服NAT问题

如果安装了Ranorex Studio的计算机和具有Ranorex代理的计算机连接到不同的网络，则此代理可能不会自动显示在你的代理列表中，你可能无法使用IP地址手动添加它。 默认情况下，计算机没有路由信息来连接到自己网络之外的计算机。

要解决此问题，必须在网络之间的网关或每台计算机上配置网络路由。

下面，我们展示了一个示例，其中Ranorex Studio和Ranorex代理安装在连接到不同网络的计算机上，并提供了如何在它们之间创建网络路由的解决方案。

![B8120-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRemote/B8120-0000050.png)  

如上图所示，我们的示例网络以192.168.x.x开头。 一个具有网关192.168.2.1，另一个具有192.168.3.1。 两个网关共享子网192.168.1.x. 该子网具有连接到Internet的网关192.168.1.1。

网关192.168.3.1的网络包含两台计算机，其中一台运行在其上的三台虚拟机（VM）。 它们都有192.168.3.x IP地址。

在192.168.2.1网络上有一台路由器，只有两台计算机。
所有这些计算机都具有192.168.2.x IP地址。

如果从计算机“192.168.3.6”（VM C）ping“192.168.2.2”（PC 2），则请求将超时，除非你在网关上启用正确的路由。 假设192.168.3.6（VM C）运行的是Windows 7，请在192.168.3.6（VM C）上键入以下命令之一：

- route add 192.168.2.0 mask 255.255.255.0 192.168.1.2 metric 2  

(add whole network to the route table)

- route add 192.168.2.2 mask 255.255.255.0 192.168.1.2 metric 2  

(add single computer to the route table)

输入命令后，ping /通信将成功从192.168.3.6（VM C）转到192.168.2.2（PC 2），但192.168.2.2（PC 2）仍然无法ping 192.168.3.6（ VM C）。 有两种解决方法可以实现这两个网络之间的通信：

- 在网关上建立一条路线
- 在需要跨网络通信的计算机上设置路由

设置路由时请考虑网关防火墙，因为它们可能会阻止来自计算机的交叉流量。 如果是这种情况，你将需要网络管理员来代替在网关上设置路由，或者设置端口转发以允许通过防火墙的流量。

由于公司internet防火墙后面的大多数网关都具有桥梁的功能，因此在本地网络上没有多少内部通信受到防火墙的保护。
要检查连接是否有防火墙，请尝试“tracert 192.168.2.2”。
如果星号“*”出现在“跟踪路由”而不是IP地址，那么连接要么通过防火墙，要么被错误地定向到internet。

请注意，在此方案中已选择标准子网：255.255.255.0
你需要确认网关两侧的子网，并根据需要调整路由设置命令。

**路由度量**（命令中的最后一个数字）被分配给路由，并用于标识其优先级 - 1具有最高优先级。 通常，网络管理员根据路由中的跳数来确定路由器度量，因为跳数最少的路由通常是最好的。 由于我们示例中的路由包含两个跃点，因此我们的路由器度量标准为2。

> **注意：**  
> 如果向其添加'-p'参数，则route命令只是持久的（它会在重启后保留）。 因此，你可以轻松地在没有风险的情况下尝试路由命令，如果你想要撤消它们，只需重新启动即可。 一旦找到了正确的路由，就可以在重启后使命令持久化。


[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorex-remote/remote-faq/
