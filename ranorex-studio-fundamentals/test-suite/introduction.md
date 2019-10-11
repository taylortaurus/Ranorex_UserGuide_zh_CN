# [译] 测试套件


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年7月8日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月5日-green.svg?longCache=true&style=flat-square)

---

测试套件是构建、组织和运行你在Ranorex Studio中测试的地方。测试套件主要由测试用例组成，而测试用例又是由模块构建的。您可以添加智能文件夹来构建您的测试。测试套件也可以配置变量和绑定数据 👉 [数据驱动测试][1]。您可以在Ranorex Studio或独立的Ranorex测试套件运行器中运行测试套件。

**本章导视**

- [下载示例解决方案](#下载示例解决方案)
- [测试套件文件](#测试套件文件)
- [测试套件视图](#测试套件视图)

>**视频向导**      
>视频“Ranorex Studio测试套件简介”将向您介绍本章中的信息。     
>[立即观看][6](视频来自Youtube)


## 下载示例解决方案

测试套件一章中的解释基于一个示例解决方案。
你可以在下面下载。

**示例解决方案** 
> 主题：测试套件  
> 时间：10min以内  
> 下载：[点我下载][2]  

**安装**

1. 解压项目目录到你的计算机任一文件夹
2. 使用RanorexStudi打开`RxDatabase.rxsln`解决方案

**贴士**  
示例解决方案适用于Ranorex版本8.0或更高版本。你需要将解决方案自动升级同意到8.2及更高版本的。

## 测试套件文件

每个测试套件包含在一个特殊的文件的扩展名`.rxtst`（Ranorex测试套件）。测试套件文件是项目的一部分，你可以在项目视图中找到。一个项目可能包含多个测试套件文件，
在你的硬盘上，测试套件文件存储在相应项目的文件夹中，例如：

`%USERPROFILE%\RanorexRanorexStudio Projects\RxDatabase\RxDatabase.rxtst`

测试套件文件是XML文件，可以在任何XML查看器或编辑器中打开。

**注意**  
> 在用户指南中，我们将为测试套件本身和.rxtst文件使用术语“测试套件”。当我们只指其中一个的时候，我们会指出来。

![A5010-0000011](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5010-0000011.png)  
*项目视图中的测试套件文件*  

### 添加一个测试套件

有些项目默认情况下不包含测试套件，或者您可能希望向项目添加多个测试套件，按照下面的说明去做。


![A5050-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5050-0000010.png)

1. 在Studio工具栏上，点击`Add test suite`按钮
2. 如果你的解决方案包含多个项目，选择一个所要添加的项目，点击`OK`
3. 在下一步对话框，赋予测试套件一个名称
4. 点击`Create`

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 测试套件 \> 👉 [管理多个测试套件][3]一文中介绍和解释了相关概念

## 测试套件视图

要打开测试套件，双击测试套件文件。出现测试套件视图，这是您在测试套件中工作的地方。

![A5010-0000021](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/TestSuite/A5010-0000021.png)

1. `ADD`按钮：单击此处可显示要添加到测试套件的下拉列表，例如测试用例或智能文件夹。您还可以通过在测试套件层次结构中右键单击添加项。如果不能在测试套件层次结构的当前级别上添加项，则下拉列表中的项将变为灰色。

2.  `RUN`按钮：点击此按钮选择的运行配置中运行测试套件

3. `run configuration`选择器：在这里您可以选择和管理运行配置(见下文)

4. `maintenance mode`开关：启用或禁用的维护模式(见下文)。

5. `MANAGE DATA SOURCES`按钮：添加和管理测试数据源，Ranorex Studio支持使用一个简单数据表，也支持链接到CVS、Excel、或是SQL数据文件。

6. 测试套件工具栏，具体包括以下内容

- 剪切/复制/粘贴/删除和取消/重做按钮
- 数据源按钮打开测试用例或智能文件夹的数据源对话框

7. 搜索框：使用搜索框来定位项目的测试套件

8. 测试套件工作空间，具体包括以下内容

- `Item`列：显示测试套件及其包含的项，在这里构建测试
- `Data binding/ iterations`列：显示应用于相应项的数据绑定和迭代(参见下文)
- `Description`列：在这里输入一个项目的可选描述，例如测试用例所涵盖的AUT方面

> **章节预览**  
> 在 \> Ranorex Studio 基础教程 \> 测试套件 \> 👉 [管理多个测试套件][4]一文中介绍和解释了相关概念

> **章节预览**  
> 在 \> Ranorex Studio 高级教程 \> 👉 [数据驱动测试][1]一文中介绍和解释了相关概念

> **章节预览**  
> 在 \> Ranorex Studio 高级教程  \> 👉 [维护模式][5]一文中介绍和解释了相关概念

---
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[测试套件结构👉][7]



[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/test-suite/introduction/
[1]: ..//..//..//ranorex-studio-advanced/data-driven-testing/introduction.html
[2]: https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleTestSuite.zip
[3]: .\multiple-testsuites.html
[4]: .\running-tests.html
[5]: ..//..//..//ranorex-studio-advanced/maintenance-mode.html
[6]:https://www.youtube.com/embed/lX4Up53NxGI
[7]:.\test-suite-structure-elements.html
