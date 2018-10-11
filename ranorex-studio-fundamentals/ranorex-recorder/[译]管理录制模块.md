# [译] 管理录制模块

*原文地址 👉 [Manage recording modules][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-10-10*    

---

在本章中，您将学习如何在Ranorex Studio中管理和构建录制内容。

**本章导视，章节内段落跳转推荐使用右上角的锚点！**  

- [重命名一个录制模块](#重命名一个录制模块)
- [剪切/复制/粘贴/删除一个模块](#剪切复制粘贴删除一个模块)
- [在文件夹中组织录制模块](#在文件夹中组织录制模块)
- [录制模块中的动作结构](#录制模块中的动作结构)
- [添加一个新的录制模块](#添加一个新的录制模块)
- [使用现有的动作上创建一个新的录制模块](#使用现有的动作上创建一个新的录制模块)

## 重命名一个录制模块

录制模块的默认名称总是`RecordingX.rxrec`，其中X为录制模块数。您可以在几个地方更改记录模块的名称。

![A4060-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4060-0000010.png)  
*更改录制模块名称*  

1. 在项目文件视图中重命名
    - 使用上下文菜单或是按F2
    - 所有关联文件的名称将自动更改
2. 在模块浏览器视图中重命名
    - 使用上下文菜单或是按F2

## 剪切/复制/粘贴/删除一个模块

使用标准Windows键盘快捷键或上下文菜单在项目视图中剪切，复制，粘贴和删除录制模块。

![A4060-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4060-0000020.png)
*剪切/复制/粘贴/删除动作元素* 

1. 在上下文菜单剪切/复制/粘贴/删除

**提示**  

你不能再模块浏览器里剪切/复制/粘贴/删除

## 在文件夹中组织录制模块

您可以在项目视图中的文件夹中组织录制模块

![A4060-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4060-0000030.png) 
*在项目视图中创建一个新的文件夹*  

1. 在项目视图中，选择要在其中创建新文件夹的项目
2. 打开上下文菜单
3. 点击`Add` > `New Folder`
4. 给文件夹一个有意义的名称（例如：`MyRecordings`）

![A4060-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4060-0000040.png)  
*将录制模块移到新的文件夹*  

5. 将录制模块拖到新的文件夹中

#### 结果

1. 项目视图中的录制模块在新的文件夹中
2. 模块浏览器的录制模块在新的文件夹中

## 录制模块中的动作结构

您可以将分隔符添加到动作表中的可视结构动作中，这纯粹是表面文章，它对操作或执行没有影响。

![A4060-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4060-0000050.png)  
*在两个动作之间添加分隔符*  

1. 点击`Add new action` > `Separator`
2. 分隔符被添加到选中的动作之后

**提示** 
> 分隔符也将在报告中显示为日志消息

![A4060-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4060-0000060.png)  
*在报告中的分隔符信息*  


## 添加一个新的录制模块

努力使您的录制模块尽可能小。这就是为什么迟早你需要额外的录制模块来保持你良好的测试结构。

![A4060-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4060-0000070.png)  
*添加一个新的录制模块*  

1. 在Studio的工具栏上，点击`Add recording module`按钮
2. 选择你要保存模块的文件夹并点击OK
3. 给模块一个有意义的名称，然后点击`Create`

## 结果

- 录制模块将会显示在项目视图和模块浏览器里

![A4060-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4060-0000080.png)
*在项目视图和模块浏览器里新的录制模块*  

1. 在项目于视图中新的录制模块
2. 在模块浏览器中新的录制模块

## 使用现有的动作上创建一个新的录制模块

有时，录制的测试可能包含太多操作。这使得录制难以重用。Ranorex Studio允许您使用移动动作到新的录制模块，将大的录制分割成模块化的、可重用的。

1. 选择要移动到新录制的动作，然后右键单击打开上下文菜单

![A4060-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4060-0000090.png)   
*移动动作到新的录制模块*  

1. 点击`Move to new recording module`。如果您有自定义文件夹，也可以选为新模块的目标文件夹
2. 给模块一个有意义的名称，
3. 然后点击`Create`

### 结果

使用所选的动作创建新的录制模块。新的模块将会出现在项目视图和模块浏览器中。

![A4060-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexRecorder/A4060-0000100.png)  
*移动动作后创建的新录制模块*  

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/ranorex-recorder/managing-recording-modules/

