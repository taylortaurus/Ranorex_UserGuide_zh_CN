# [译] 快照文件


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月19日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年10月9日-green.svg?longCache=true&style=flat-square)


---

Ranorex快照是在特定时间点被测试应用程序(AUT)的用户界面(UI)结构的文件表示。Ranorex快照捕获所有接口元素、它们的层次结构、值等。

它可以保存为单个文件。可以使用Ranorex Spy创建和查看Ranorex快照文件。文件扩展名是`.rxsnp`。

通常，Ranorex快照用于与Ranorex支持和技术销售团队共享应用程序UI的详细信息。

**本章导视**

- [创建一个标准的快照文件](#创建一个标准的快照文件)
- [创建隐藏的UI元素的快照](#创建隐藏的UI元素的快照)
- [加载快照文件](#加载快照文件)


>**视频向导**     
截屏视频“快照文件”将引导您了解本章中的信息。            
[立即观看](https://www.youtube.com/embed/Tx1PdLwgC9o)

## 创建一个标准的快照文件
标准快照文件捕获的UI不包含菜单，菜单项，上下文菜单，工具提示等隐藏的UI元素。下面的下一个主题将说明创建包含这些元素的UI快照。

要创建标准快照文件：

1. 启动您的AUT（例如Ranorex Studio演示应用程序）。

2. 启动 Ranorex Spy。

![B4040-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4040-0000010.png)


3. 使用TRACK按钮，在AUT中跟踪 UI元素（例如，如下所示的Submit按钮）。

![B4040-0000020](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4040-0000020.png)

4. 在元素树浏览器的工具栏中，单击 “ 另存为快照...”按钮。

5. 命名文件并指定保存位置。

6. 单击“Save”开始创建并保存快照文件。


**注意**
>快照文件的默认保存位置为%USERPROFILE%\RanorexSnapshots。

![B4040-0000030](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4040-0000030.png)

7. 创建快照时，进度条将指示进度。完成后，将显示以下消息。单击close。

![B4040-0000040](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4040-0000040.png)


**注意**
>快照通常包含的跟踪/选择的UI元素和完整的祖先子树，即，相应的应用程序的所有元素。您可以在“Settings”>“Advanced”>“让快照包含完整的祖先子树”下更改此默认行为。

>**章节预览**      
有关高级设置的说明，请参见             
Ranorex Studio系统详细信息>设置和配置>[👉高级设置和配置][1]。

## 创建隐藏的UI元素的快照
某些UI元素（例如，下拉菜单，弹出窗口，组合框等）仅在诸如单击之类的交互之后可见，并且通常在AUT失去焦点时消失。这些元素是“隐藏的”，因此不会自动包含在快照文件中。这是因为它们在Ranorex Spy中作为单独的项目显示在元素树的顶层。将这些元素捕获到快照文件中需要使用即时跟踪功能。

>**章节预览**      
跟踪隐藏的UI元素的说明如下               
Ranorex Studio高级>跟踪UI元素>[👉即时跟踪][2]。               
替代方法在             
Ranorex Studio高级>跟踪UI元素>[👉跟踪按钮][3]。

要创建具有隐藏UI元素的快照文件，请执行以下操作：

1. 启动您的AUT并导航到要跟踪的隐藏UI元素出现的位置（例如，在“演示应用程序”的“测试数据库”选项卡中）。

2. 启动 Ranorex Spy。

![B4040-0000050](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4040-0000050.png)


3. 使隐藏的UI元素可见（例如，通过打开包含的下拉菜单，如“演示应用程序”中的“项目管理”列表项一样），并确保其处于焦点（例如，将鼠标悬停在其上）。

4. 突出显示UI元素后，按Ctrl + WIN。

5. 跟踪的UI元素出现在Spy的元素树中。

![B4040-0000060](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4040-0000060.png)

6. 现在，在执行其他操作之前，请按Scroll键 以创建先前跟踪的隐藏UI元素及其祖先子树的快照，并将其缓存到工作内存中。

![B4040-0000070](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4040-0000070.png)


1.快照文件已成功创建并缓存到工作内存中。在这种情况下，快照文件中打包了10个UI元素，该文件现在已在Ranorex Spy中打开。

2.警告快照文件可能不完整。当您尝试不使用Scroll创建隐藏的UI元素的快照时，通常会发生这种情况。

7. 快照文件会在Ranorex Spy中自动打开。状态消息从“LIVE”切换到“SNAPSHOT”表示。

![B4040-0000080](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4040-0000080.png)


### **保存快照文件**

最后，您需要将Scroll创建的快照从工作内存保存到永久存储。

7. 在元素树工具栏中，单击 “ 另存为快照...”按钮。

8. 命名文件，指定保存位置，然后单击“保存”。

![B4040-0000090](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4040-0000090.png)

9. 一条消息显示快照文件已成功保存。

![B4040-0000100](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4040-0000100.png)


## 加载快照文件
您也可以在Ranorex Spy中加载快照文件。

为此：

1. 启动 Ranorex Spy，然后在元素树工具栏中，单击 “ 从快照加载...”按钮。

2. 浏览到要打开的快照文件。

3. 单击Open
   
![B4040-0000110](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4040-0000110.png)                       
*加载快照–第一部分*

1. 启动Ranorex Spy，然后单击工具栏中的“从快照加载...”。
2. 选择文件夹并保存快照文件
3. 单击“ 打开”。

**注意**
>快照文件的默认保存位置为%USERPROFILE%\RanorexSnapshots。

4. 快照文件在Spy中打开，如新元素树所示，状态指示器从LIVE变为SNAPSHOT。

![B4040-0000120](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B40/B4040-0000120.png)

1. 状态指示器，显示快照文件的创建日期。

---

[👈路径编辑器][4]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[GDI捕获功能👉][5]



[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorex-spy/snapshot-files/
[1]: ..\\..\\ranorex-studio-system-details/settings-configuration/advanced-settings-configurations.html
[2]: ..\\..\\ranorex-studio-advanced\tracking-ui-elements/instant-tracking.html
[3]: ..\\..\\ranorex-studio-advanced\tracking-ui-elements/track-button.html
[4]:.\the-path-editor.html
[5]:.\gdi-capture-feature.html