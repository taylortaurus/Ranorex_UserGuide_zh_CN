# [译] 用户代码动作

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月9日-green.svg?longCache=true&style=flat-square)


---
用户代码动作扩展了基本和智能动作的功能。示例包括自定义验证，访问与测试用例相关的数据和参数以及扩展报告。

在本章中，您将学习如何 在actions表中管理用户代码动作。编写自己的用户代码需要编程知识，因此超出了本章的范围。您可以然而利用其他人通过用户代码库编写的用户代码动作。

>**章节预览**    
用户代码库是Ranorex Studio专家>用户代码库> 👉[简介]中介绍的专家主题。


**本章导视**


- [找到用户代码文件](#找到用户代码文件)
- [查看基础动作代码](#查看基础动作代码)
- [将标准动作转换为用户代码](#将标准动作转换为用户代码)
- [用户代码动作和参数](#用户代码动作和参数)
- [用户代码返回值](#用户代码返回值)
- [将动作合并到用户代码动作中](#将动作合并到用户代码动作中)


>**视频向导**    
视频“用户代码动作”将引导您完成本章中的内容。    
[立即观看](https://www.youtube.com/embed/pq1kpyqVX4g)

## 找到用户代码文件
每个录制模块由三个文件组成。您可以在Ranorex Studio的项目视图中找到这些文件，也可以直接在项目文件夹中的硬盘驱动器上找到这些文件。**双击**打开它们。

![A6070-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6070-0000010.png)        
*录制模块 - 代码文件*

1. 在Recorder视图中具有控件库的动作表。
2. 录制模块的代码表示。
- 机器生成的录制模块的代码表示。
- 由Ranorex自动更新。您所做的任何修改都将被丢弃。
- 只读。
3. 录制模块的用户代码表示。
- 用于录制模块和用户代码动作的用户代码文件。
- 将所有用户代码写入此文件。
- 用户代码库中的用户代码方法将自动添加到此文件中。
- 
## 查看基础动作代码

要查看动作的基础代码：

![A6070-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6070-0000020.png)       
*查看动作代码*

1. 选择一个动作。

2. 右键单击它并单击“view code”，或按 Ctrl +  Enter。

3. 出现动作的代码。

>**贴士**     
该文件已被锁定，因此您无法更改它。它由Ranorex自动更新。


## 将标准动作转换为用户代码
您可以将标准动作转换为用户代码动作。

为此：

![A6070-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6070-0000030.png)       
*转换为用户代码动作*

1. 右键单击某个动作。
2. 单击convert to user code。
3. 该动作显示为具有默认方法名称的用户代码动作。
4. 双击用户代码动作以在代码编辑器中查看其代码。

![A6070-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6070-0000040.png)        
*示例用户代码动作*

## 用户代码动作和参数
您可以在参数编辑器或代码中为用户代码动作配置参数。

![A6070-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6070-0000050.png)     
*用户代码动作参数和参数*

1. 用于打开代码方法的参数编辑器的按钮。
2. 论证编辑。
3. 动作代码中的参数。


参数名称：

- 可以是任何名字。
- 使用命名约定是最好的，尤其是在团队中工作时。
  
可用的参数类型：

- String（value）可以绑定到变量
- Boolean（true，false）可以绑定到变量
- DateTime（值“YYYY / DD / MM”）可以绑定到变量
- 持续时间（以ms为单位的值）可以绑定到变量
- Int32（整数值），可以绑定到变量
- 位置（值中心，中间，......）可以绑定到变量
- 点（坐标值）可以绑定到变量
- Rectangle（维度值），可以绑定到变量
- TimeSpan（时间格式），可以绑定到变量
- Double（double value），可以绑定到变量
- 适配器（Ranorex适配器），链接到控件库项目
- RepoItemInfo（控件库项），链接到控件库项


## 用户代码返回值
默认情况下，用户代码方法不返回值。但是，您可以将其中一个可用数据类型指定为方法返回值。

为此：

1. void用您想要的数据类型替换默认返回值。

2. 添加一行以返回指定的值。

![A6070-0000052](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6070-0000052.png)

3. 这会导致返回值列显示在动作表中。它包含用户代码方法的返回值，并允许您使其变量。

![A6070-0000054](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6070-0000054.png)

或者，您可以使用上下文菜单创建具有返回值的用户代码方法：

1.右键单击某个动作。

2.单击转换为具有返回值的用户代码。

3.新动作将显示在动作表中，包括“return value”列

![A6070-0000056](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6070-0000056.png)

## 将动作合并到用户代码动作中
可以将两个或多个动作合并为单个用户代码动作，如下所示：

![A6070-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6070-0000060.png)        
*将动作合并到用户代码*

1. 选择要合并的动作。
2. 右键单击它们以打开上下文菜单。

a. 单击“将项目合并到用户代码项”以创建不带返回值的默认用户代码方法。

b. 单击“将项目合并到具有返回值的用户代码项”以创建具有返回值的用户代码方法。

3. 给新用户代码的动作命名并按 Enter键。


### **结果**：
动作代码显示在新用户代码动作的代码中。

![A6070-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6070-0000070.png)        
*用户代码中的合并动作*


1. 默认合并用户代码方法，不带返回值
2. 合并用户代码方法的Boolean返回值。

---
[👈调用动作][2]



[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/actions/user-code-actions/
[1]:.\ranorex-studio-expert\user-code-library\introduction.html
[2]:.\invoking-actions.html

