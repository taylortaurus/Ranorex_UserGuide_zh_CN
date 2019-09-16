# [译] Git

*原文地址 👉 [Git][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-17*    

---

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [关于Git和Ranorex Studio](#关于Git和RanorexStudio)
- [添加Ranorex解决方案到Git](#添加Ranorex解决方案到Git)
- [从Git上检出一个Ranorex解决方案](#从Git上检出一个Ranorex解决方案)
- [项目视图中叠加的图标意义](#项目视图中叠加的图标意义)  

## 关于Git和RanorexStudio

Git是一种免费的、开源的、分布式版本控制系统。为了在Ranorex Studio中使用Git，必须按给定顺序执行以下先决条件：

- Git需要安装
    - Windows版的Git在这里下载安装 👉 [https://git-scm.com/download/win][1]
    - 请确保在Git安装期间选择`从Windows命令提示符使用Git`!

![E4010-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000010.png)  

- TortoiseGit需要安装
    - 在这里下载TortoiseGit 👉  [https://tortoisegit.org/download][2]
    - TortoiseGit是Git的Windows shell界面，例如，需要覆盖显示文件状态的图标。

Ranorex Studio将帮助你完成此对话框，以防机器上没有所需的先决条件：

![E4010-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000020.png)  


## 添加Ranorex解决方案到Git


请确保你的Git基础结构已经建立并运行。

要将现有的Ranorex解决方案添加到Git，请打开解决方案的上下文菜单。转到`Source Control`，选择`Add Solution to Source Control`。

![E4010-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000030.png)  

要向Git添加一个新的Ranorex解决方案，请在“new Project”对话框中选中“add To Source Control”选项。

![E4010-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000040.png)  

“源代码管理向导”将被打开。
请遵循以下说明:

1. 选择Git作为源代码控制提供程序

![E4010-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000050.png)

2. Ranorex解决方案被自动配置为一个新的本地Git仓库。在项目视图中，所有文件都用加号表示

![E4010-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000060.png)  

3. 要将当前状态提交到本地存储库，请单击解决方案上下文菜单中的`commit`

![E4010-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000070.png)  

4. 提交之后，项目视图中显示一个检查符号

![E4010-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000080.png)  

所有进一步的Git相关步骤都应该在你的工作流中定义  


## 从Git上检出一个Ranorex解决方案


请确保你的Git基础结构已经建立并运行

1. 操作步骤 `Tools` > `Source Control` > `Checkout`

![E4010-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000090.png)  

2. 在源代码控制向导中选择Git

![E4010-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000050.png)

3. TortoiseGit将询问你存储库的路径以及你希望在本地计算机上存储文件的位置。填写到Git存储库的URL以及到本地目录的路径，然后单击OK。

![E4010-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000100.png)  

4. 整个存储库将被克隆到本地文件夹中。克隆成功后，将显示此对话框。

![E4010-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000110.png)  

5. 如果你的存储库在其根目录中包含Ranorex解决方案，则该解决方案将自动打开。如果不是这样，你必须从文件系统手动打开Ranorex解决方案。

从本地文件夹中打开Ranorex解决方案后，你将看到项目视图中叠加的图标。

![E4010-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000080.png)  

所有进一步的Git相关步骤都应该在你的工作流中定义


## 项目视图中叠加的图标意义


将叠加图标添加到Ranorex Studio的Projects视图中，因为解决方案在源代码控制之下

|图标|说明|
|:--|:--|
|![icon_normal][icon_normal] `Normal`|没有本地修改，没有等待提交的更改|
|![icon_conflicted][icon_conflicted]`Conflicted`|说明有冲突|
|![icon_modified][icon_modified]`Modified`|等待提交的修改|
|![icon_added][icon_added]`Added`|标记为添加，等待提交|

[0]: https://www.ranorex.com/help/latest/interfaces-connectivity/source-control-revision-control/git/
[1]: https://git-scm.com/download/win
[2]: https://tortoisegit.org/download
[icon_normal]: https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000120.png
[icon_conflicted]: https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000130.png
[icon_modified]: https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000140.png
[icon_added]: https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/E4010-0000150.png

