# [译] 构建控件库项目
    

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月9日-green.svg?longCache=true&style=flat-square)

---
 随着测试套件变得越来越大，越来越复杂，您的控件库也将包含越来越多的项目。通常，它们是自动构建的，即Ranorex Studio将自动创建app folder和rooted folder。但是，这可能会使许多项目变得混乱。您可能更喜欢自己构建控件库。本章介绍可用文件夹的类型以及如何使用它们构建您的控件库。

 
**本章导视**


- [App文件夹](#App文件夹)
- [根文件夹](#根文件夹)
- [简单文件夹](#简单文件夹)



---

>**视频向导**      
视频“构建控件库项目”将引导您完成本章中的内容。    
[立即观看](https://www.youtube.com/embed/qYYEDzw1fuU)

## App文件夹
app文件夹是根文件夹。它们表示控件库元素的树结构中的顶级数据容器。他们永远不可能是另一个文件夹的子文件夹。在下面的示例中，文件夹RxMainFrame和List1000是app文件夹。

![A7050-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7050-0000010.png)

1. RxMainFrame

- RxMainFrame是包含Ranorex Studio演示应用程序的所有UI元素的顶级文件夹。
  
2. List1000

- List1000是顶级文件夹，其中包含“部门”下拉列表中的所有可选项。


>**贴士**         
要使用app文件夹，您需要对👉UI元素和👉RanoreXPath有基本的了解。

### **创建一个app文件夹**

![A7050-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7050-0000020.png)

1. 在“Item”列中，右键单击空白区域。

2. 点击Add new item > app folder或按Ctrl键 + P。

3. 新的app文件夹将显示默认名称。

>**贴士**       
您还可以单击控件库视图的菜单栏中的Add new item  >  App foldee。

### **重命名app文件夹**

![A7050-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7050-0000030.png)     
*重命名app文件夹*

1. 选择所需的app文件夹，然后按 F2。

2. 输入名称。
 
>**贴士**          
请注意，controlname控件库项目的路径中的内容保持不变。仅更改控件库中的显示名称。

## 根文件夹
根文件夹表示UI的不同部分，其中包含一组单独的UI元素。根文件夹中的控件库项目都共享相同的基本路径，即根文件夹的路径。在下面的示例中，  RxTabStandard是一个根文件夹。

![A7050-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7050-0000040.png)  

1. RxTabStandard

- 根文件夹及其在演示应用程序的UI中表示的内容，即“测试数据库”选项卡。
- 根文件夹中的所有项共享根文件夹的路径。
2. 根文件夹中的控件库项目

- 表示测试数据库选项卡左侧部分中UI元素的控件库项目，后者又由根文件夹表示。

### **创建一个rooted文件夹** 

![A7050-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7050-0000060.png)


1. 右键单击要添加根文件夹的位置。

2. 单击“add new item”。

3. 点击根文件夹，或按Ctrl键 + R 。

>**贴士**        
您还可以单击控件库视图菜单栏中的添加新项目> Rooted文件夹。

### **将项目分组到新的有根文件夹中**

您还可以将现有控件库项目分组到新的根文件夹中。

![A7050-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7050-0000070.png)

1. 选择要分组的控件库项目。

2. 右键单击它们，然后单击`Group in new rooted folder`。

3. 命名文件夹。控件库项目分组在新文件夹中。

1.分组控件库项的路径规范

- rooted文件夹的路径是所选控件库项的共享路径。
- 控件库项目以其各自的路径结尾显示。



### **重命名根文件夹**

![A7050-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7050-0000050.png)


1. 单击所需的根文件夹，然后按 F2。

2. 输入名称。

### **优化文件夹的路径**
根节点文件夹的路径应始终是它包含的所有控件库项目之间共享的最长路径。要确保这种情况，请使用“优化文件夹路径”选项。

![A7050-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7050-0000080.png)

1. 根文件夹SelectGender及其两个控件库项ButtonFmale和ButtonMale。

2. 根文件夹的基本路径为空。

3. 两个控件库项的完整路径。请注意，它们仅在末尾的控件名称上有所不同。

![A7050-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7050-0000090.png)

1. 右键单击根文件夹。

2. 单击Optimize folder path。

![A7050-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7050-0000100.png)

1. 同样，相同的根文件夹SelectGender及其两个控件库项ButtonFmale和ButtonMale。

2. 根文件夹的基本路径现在是两个控件库项目的最长共享路径。

3. 仅显示唯一标识两个控件库项所需的路径部分。

## 简单文件夹
简单文件夹没有基本路径。这些文件夹允许您使用自己的逻辑类别，例如Windows中的文件夹。永远不会自动创建简单文件夹。需要手动创建和管理它们。

![A7050-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/Repository/A7050-0000110.png)         
*创建一个简单文件夹*

1. 右键单击要添加简单文件夹的位置。

2. 单击Add new item > Simple folder或按 Ctrl键 + d。

3. 命名该文件夹并用控件库项填充它。

---

[👈管理控件库项][1]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[清理控件库👉][2]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/repository/structuring-repository-items/

[1]:.\managing-repository-items.html
[2]:.\repository-cleanup.html