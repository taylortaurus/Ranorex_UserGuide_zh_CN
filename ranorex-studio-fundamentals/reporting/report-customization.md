# [译] 定制化报告

*原文地址 👉 [Report customization][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-25*    

---

标准报告通常适用于大多数情况。 但是，为了满足个人需求，它是完全可定制的。 我们将选项分为两个章节，一个用于更简单的自定义，另一个用于更复杂的自定义。 在本章中，你将学习有关自定义的基础知识，主要是如何更改报告的外观，即添加自己的logo和更改模板。

> **章节预览**  
> 有关涉及编码的更复杂的自定义，请参阅 \> Ranorex Studio 基础教程 \> 报告 \> 👉 [复杂自定义][1]  

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [下载示例解决方案](#下载示例解决方案)
- [从原始数据到报告](#从原始数据到报告)
- [创建一个自定义报告模板](#创建一个自定义报告模板)
- [多个自定义报告模板](#多个自定义报告模板)
- [重命名自定义报告模板](#重命名自定义报告模板)
- [选择/重新应用报告模板](#选择/重新应用报告模板)
- [重置到默认报告模板](#重置到默认报告模板)
- [Ranorex如何处理自定义模板](#Ranorex如何处理自定义模板)
- [在报告中包含外部文件](#在报告中包含外部文件)
- [背景颜色和logo自定义](#背景颜色和logo自定义)
- [用用户名替换计算机/端点](#用用户名替换计算机/端点)
- [更改报告消息格式](#更改报告消息格式)
- [从报告中删除信息](#从报告中删除信息)

## 下载示例解决方案

本章中的说明基于下述下载的示例解决方案。

**练习，我能做什么？** 
> 主题：报告自定义  
> 时间：15min以内  
> 下载：[点我下载][1]  

**安装**

1. 解压项目目录到你的计算机任一文件夹
2. 使用RanorexStudi打开`RxDatabase.rxsln`解决方案

**贴士**  
示例解决方案适用于Ranorex版本8.0或更高版本。你需要将解决方案自动升级同意到8.2及更高版本的

## 从原始数据到报告

下面的图片说明了在报表中以易于阅读的格式显示原始数据的过程。

![A9050-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000010.png)  
*Ranorex报告的概念*

1. 在测试运行期间，报表引擎以XML格式收集数据。
2. 接着报表引擎将此数据转换为HTML，并根据CSS和XSL规范创建报表文件。
3. 然后，Ranorex Studio可以使用其内置的HTML查看器显示此基于HTML的报告。

### 收集的测试数据

收集测试运行的数据并以XML格式存储。此原始数据也可以在Ranorex Studio外部使用任何XML查看器/编辑器进行读取和使用。

![A9050-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000020.png)  
*XML格式的测试数据* 

原始XML数据总是保存在和对应报告相同的文件夹中，并且具有相同的文件名和添加的后缀`.data`

![A9050-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000030.png)  
*报告文件和XML数据文件*  

### CSS和XSL格式

然后使用原始XML数据创建基于CSS和XSL规范的HTML文件。

![A9050-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000040.png)  
*用于生成HTML文件的XSL和CSS格式也存储在与XML数据和实际报告相同的文件夹中*  

![A9050-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000050.png)  
*CSS和XSL文件*  

> **章节预览**  
> 为了能够更改Ranorex标准报告的布局和内容，建议你对HTML，CSS，XSL和XML有基本的了解。 有关详细信息，请参阅[www.w3.org][2]上的万维网联盟（W3C）

### HTML报告文件

由XSL和CSS从XML生成的最终报告是基于HTML的格式存储在项目目录的Reports文件夹中。

![A9050-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000060.png)  
*基于html的报告文件和报告显示在Ranorex Studio*

**提示**  
> - 报告可以在任一Web浏览器中查看
> - 报告文件可以在任一HTML编辑器里编辑

## 创建一个自定义报告模板

现在我们已经确定了如何生成报告，现在我们可以开始自定义报告了。在Ranorex Studio中有一种方便的方法可以在不影响标准报告的情况下执行此操作：

1. 在测试套件视图，`右键`测试套件
2. 点击`Properties`
3. 点击`Report`选项卡

![F3040-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/F3040-0000010.png)  

4. 点击`Create custom template`
5. 将显示一条消息，告诉你新报告模板文件夹的创建位置，单击确定确认。


![A9050-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000070.png)  

### 结果

在项目视图中，在项目视图中，你可以看到包含复制的报告文件的新模板文件夹。

![A9050-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000080.png)  
*项目视图中的NewCustomTemplate1文件夹*

1. CSS、XSL和图像文件
    -  这些是你更改的复制文件，用于自定义报告的布局和内容
    -  PNG文件包含Ranorexlogo作为报告的默认logo以及标准报告中使用的其他图像，你可以用自己的图像替换它们
2. 预览文件
    - 这些文件使你能够快速检查在实际报告中其他文件中的定制是什么样子的。打开视图，获得预览
    - 你也可以从Windows打开它，因此你不必启动Ranorex Studio

## 多个自定义报告模板

你可以根据需要创建任意数量的自定义报告模板。 但是，测试套件一次只能激活一个模板。要创建其他自定义模板：

1. 在测试套件属性的`Report`选型卡中，点击重置到默认
2. 再点击`Create custom template`并点击`OK`

![A9050-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000090.png)  

## 结果

另一个模板文件夹出现在项目视图中。

![A9050-0000091](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000091.png)  
*多个自定义报告模板的示例*


## 重命名自定义报告模板

你可以重命名自定义报告模板

1. 在项目视图中，选择你要重命名的模板
2. 按下`F2`可以重命名模板文件夹
3. 重命名文件夹

**注意**  
> 报告引擎不会自动识别名称更改。重命名后，你必须应用模板。  

![A9050-0000130](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000130.png)  
*重命名一个自定义报告模板*  

![A9050-0000140](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000140.png)  
*如果模板没有应用将会报错*  


## 选择/重新应用报告模板

这个功能有三种用途：

- 在文件夹中添加一个现有的自定义模板
- 如果你有多个自定义模板，选择一个并应用一个使用
- 如果你重命名了一个模板并应用了它，Ranorex可以再次找到它


**提示**  
> 同一时间，一个测试套件，只有一个报告模板是激活的

1. 在测试报告属性中打开报告选项卡
2. 如果当前有一个自定义模板处于激活状态，单击`Reset`重置到默认模板

![A9050-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000100.png)  

3. 点击`Choose custom template`
4. 在浏览视图中选择一个自定义模板
5. 点击OK

## 重置到默认报告模板

如果你想停止使用自定义模板，你可以随时重置到默认的Ranorex模板。

1. 在测试套件属性中的打开报告选项卡
2. 点击`Reset`重置到默认并确认OK

![A9050-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000110.png)  

**提示**  
> 此操作不会删除自定义报表模板。你仍然可以按照上面一节描述的那样重新应用它们

![A9050-0000120](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000120.png)
*Ranorex标准报告模板*  


## Ranorex如何处理自定义模板

Ranorex有一个特殊的机制来处理定制的报表模板。它涉及到每个项目都有的输出文件夹和报告文件夹。当你想要在报表模板中包含外部文件时，了解这个过程是很重要的，例如包含你标识的PNG，因为这些文件默认情况下不包含在这个过程中。

### Ranorex 输入文件夹 /bin/Debug

在运行测试时，Ranorex将测试运行所需的所有文件复制到指定的名为`/bin/Debug/`的输出文件夹中，该文件夹位于项目的文件夹中。报告文件也在复制的文件中，它们是从`/Reports/`文件夹中取的。外部文件，例如logo不会被复制到输出文件夹，除非它们被配置成这样，因此默认情况下不会出现在报表中。

![A9050-0000150](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000150.png)
*Ranorex输出文件夹*  

1. 自定义的报告模板文件夹（示例中的"FrogConsulting"）
2. 报告文件（.rxlog）和元数据文件（.rxlog.data）
3. CSS和XSL格式文件和另外自定义报告文件（例如，RanorexReport.png的logo文件）

**提示**  
> Ranorex在每次后续测试运行时同步输出文件夹的所有文件。

## 报告文件夹 /Reports/

在运行测试时，Ranorex还将报表文件(无论是默认的还是自定义模板)复制到/Reports/文件夹，然后将它们复制到输出文件夹。在这种情况下，外部文件如logo也会被复制。

![A9050-0000160](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000160.png)  

1. 报告文件（.rxlog）和元数据文件（.rxlog.data）
2. CSS和XSL格式文件和另外自定义报告文件（例如，RanorexReport.png的logo文件）

## 过程总结

下面的图片和描述说明了这个过程。如前所述，外部文件需要在流程中包含特殊的配置。在这种情况下，我们假设已经这样做了。你可以在下面进一步了解如何做到这一点。

![A9050-0000170](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000170.png)  

1. 你已经创建了一个定制的报告模板，并将其应用到测试套件中。自定义模板的文件夹位于项目的文件夹`FrogConsulting`中。在运行测试套件时，报表文件(CSS、XSL和自定义文件)将从这个模板文件夹复制到`/Reports/`文件夹。

2. 在第一次测试运行时，报表文件从`/Reports/`文件夹复制到输出文件夹`/bin/debug/`。在随后的运行中，这两个文件夹是同步的，即输出文件夹总是包含来自`/Reports/`文件夹的最新文件。

**贴士**  
> 为了避免旧报告的样式被“覆盖”，可以使用压缩报告。

## 在报告中包含外部文件

默认情况下，Ranorex仅在报告过程中包含内部文件（.rxlog，rxlog.data，.css，.xsl），即仅将这些文件复制到输出文件夹。对于要在自定义报告中显示的外部文件（如logo），你需要手动将它们包含在此过程中。

1. 将外部文件复制到你希望它们所属的自定义报告模板的文件夹中。
2. 在Ranorex Studio的项目视图中，单击刷新按钮以在模板的文件夹中查看该文件。

![A9050-0000180](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000180.png)  
*项目文件视图工具栏中的“刷新”按钮*  

3. 右键外部文件
4. 点击`Include in project`
5. 该文件现在包含在项目中，但我们还没有完成

![A9050-0000190](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000190.png)  

1. 复制到自定义报表文件夹中的任何文件最初都不是项目的一部分，这意味着它们也不包括在报表过程中

6. 选择外部文件并点击`F4`打开它的属性
7. 你可以看到`Copy to output folder`被设置成`Never`，因此文件仍然不会包含到报告过程中。将它更改为`Always`或是`Preserve newest`。

![A9050-0000200](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000200.png)  

1. `Never`--是任何新包含的外部文件的默认设置。
2. `Always`--表示文件将被复制到每个测试运行的输出文件夹中。
3. `Preserve newest`--表示只有在`/Reports/`文件夹中的版本比输出文件夹中的现有版本更新时才会复制该文件。如果输出文件夹中尚不存在任何文件，则始终会复制该文件

## 背景颜色和logo自定义

在此示例中，你将更改报告的背景颜色，并将Ranorex logo替换为自定义logo。该示例可在本章开头下载。

### logo

- 你的logo不必是特定尺寸，可以尝试不同的尺寸
- logo中使用的颜色是十六进制值

我们准备了一个标志样品。绿色背景有十六进制值：`#ACDB6B`

![A9050-0000210](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000210.png)  

示例logo已位于FrogConsulting自定义报告模板文件夹中

![A9050-0000220](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000220.png)  

### 替代logo

要替换logo，你需要更改CSS文件。

1. 在项目视图中，双击CSS规范文件
2. 它将在新选项卡中打开

![A9050-0000230](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000230.png)  

3. 滑到文件的末尾，找到自定义区域
4. 删除此行以取消注释自定义部分，然后按如下所述替换其内容

![A9050-0000240](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000240.png)  

1. 背景自定义
    - 背景颜色设置为与logo背景颜色相同的绿色十六进制值
    - 所有其他设置都保持不变
2. 自定义logo
    - logo的高度和宽度设置为各自的值（请参阅logo大小）
    - 默认logo名称将替换为“frogconsulting.png”
    - 其他设置保持不变
3. 报告信息框对齐方式
    - 最后，为一般信息框设置了40px的上边距 

### 结果

![A9050-0000250](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000250.png)  

**提示**  
> 如果报告中缺少logo，请记住在项目和报告过程中包含logo文件，如上所述

## 用用户名替换计算机/端点

还有各种更改报告内容的选项。我们将通过三个示例介绍基本原理，并根据你自己的想法帮助你自定义报告。在第一个示例中，你将自定义报告，以便“计算机/端点”条目显示“用户名”，而不是计算机名称显示用户名。

![A9050-0000260](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000260.png)  
*用用户名替换计算机/端点*  

1. XSL文件中定义条目标题的行。
2. 原始数据文件中的“主机”行。 它包含实际的计算机/端点名称。
3. XSL文件中的行，它从原始数据文件中的“主机”行获取计算机/端点名称，并将其显示在报告中的“计算机/端点”条目下方。

要用“用户名”替换“计算机/端点”条目并显示用户名：

1. 在XSL文件中，使用"Frog user"替代"计算机/端点"
2. 也可以在XSL文件中，使用@user替换@host变量

![A9050-0000270](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000270.png)  
*报告用户名自定义* 

3. 保存关闭文件

![A9050-0000280](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000280.png)  
*自定义用户名的报告*  

## 更改报告消息格式

在此示例中，你将更改特定类型的报告消息的格式。

如下图所示，在默认报告中，具有“成功”级别的消息以绿色字体打印。我们将其更改为粗体蓝色字体。

![A9050-0000290](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000290.png)  

#### 1. 默认成功的信息绿色的

1. 打开CSS文件
2. 找到成功消息的颜色定义并复制它
3. 将其粘贴到CSS文件末尾的定制部分，并像在图像中一样修改它
4. 保存并关闭文件

![A9050-0000300](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000300.png)

##### 2. 成功消息的默认字体颜色定义

##### 3. 自定义部分中的新颜色定义，覆盖默认定义。

**提示**  
> 不要更改默认定义（CSS行＃197 - ＃199）,这样，你就可以轻松恢复默认值。

### 结果

![A9050-0000310](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000310.png)  

## 从报告中删除信息

在本例中，你将从报表中删除信息。当某些内容不相关并且你想在报告中释放空间时，这是非常有用的。

在我们的示例中，我们希望删除报表消息的Time列

![A9050-0000320](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000320.png)  

1. 打开XSL文件
2. 找到文件中所有`Time`的实例

![A9050-0000330](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000330.png)  

#### 1. 这些行定义了XSL文件中的Time列。

3. 通过如下注释来停用所有这些

![A9050-0000340](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000340.png)  

#### 2. 此代码获取每个操作行的时间值，并将它们显示在正确的位置。

4. 通过如下注释将其取消激活

![A9050-0000350](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000350.png)


### 结果

![A9050-0000360](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Reporting/A9050-0000360.png)  
*自定义报告没有时间列*  


[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/reporting/report-customization/
[1]: https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleCustomReport.zip
[2]: http://www.w3.org/
