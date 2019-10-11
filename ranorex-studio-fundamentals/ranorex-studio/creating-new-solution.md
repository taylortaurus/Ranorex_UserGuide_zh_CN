# [译] 创建新的解决方案


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月20日-green.svg?longCache=true&style=flat-square)



---
在Ranorex Studio中，解决方案是包含所有其他测试文件的顶级容器。解决方案组织成一个或多个项目。Ranorex Studio中有不同的项目类型，但测试套件项目通常用于构建测试。测试套件项目包含一个或多个测试套件，这些测试套件又代表测试结构及其测试用例和模块。

在本章中，您将学习如何创建一个新的解决方案来测试桌面应用程序。您创建的新解决方案始终带有测试套件项目。

>**章节预览**                 
>如果要将项目添加到现有解决方案，请参阅      
>Ranorex Studio基础知识> Ranorex Studio> 👉[创建一个新的测试项目][2]              
如果要为Web或移动测试创建解决方案，请参阅                        
Web和移动测试>  [👉Web测试][3]   以及                     
网络和移动测试>  [👉Android测试][4] / [👉iOS测试][5]

**本章导视**
- [RocketStart解决方案向导](#RocketStart解决方案向导)
- [选择要测试的应用程序](#选择要测试的应用程序)
- [选择录制动作](#选择录制动作)
- [终端窗口和教程面板](#终端窗口和教程面板)
- [桌面解决方案及其项目的结构](#桌面解决方案及其项目的结构)
- [StartAUT和CloseAUT模块](#StartAUT和CloseAUT模块)




## RocketStart解决方案向导



1. 单击文件>新建>使用向导解决方案...以打开RocketStart解决方案向导。在出现的对话框中，  单击“桌面”。

2. 配置您的解决方案（参见下面的解释）; 然后  单击继续。

![](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/A30/A3040-0000011.png)       
*测试创建对话框*


1. 解决方案名称
- 为解决方案提供有意义的名称或使用默认名称。
- 默认情况下，解决方案名称也用作此解决方案中测试套件项目的名称。

2. 位置

- 除非更改，否则将在中创建新项目目录 \Ranorex\RanorexStudio Projects\

3. 单击其他选项以访问更多选项：

![](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/A30/A3040-0000021.png)

4. 如上所述，默认情况下，测试套件项目名称与解决方案名称相同。您可以在此处为项目指定其他名称。
5. 项目的编程语言。C＃是默认的，VBNet也可用。

6. 取消选择后，解决方案文件将保存在项目的文件夹中，而不是保存在项目文件夹的父文件夹中。

7. 如果需要，选中此框以将解决方案和项目添加到👉[源代码管理系统][11]。


>**视频向导**              
观看视频“改进的启动和关闭AUT动作”，了解版本9.1如何提高测试和解决方案向导的稳定性。     
[立即观看](https://www.youtube.com/embed/75uTKNy44mU)

## 选择要测试的应用程序

1. 选择一个：

a. 单击“运行应用程序”并选择一个列出的应用程序

b. 单击“浏览应用程序”>“浏览” 应用并使用Windows资源管理器浏览到应用程序。

2. 单击`Continue`

![](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/A30/A3040-0000031.png)


1. 桌面运行中的应用程序的列表。

2. 用于浏览应用程序并指定可选命令行参数的部分。


## 选择录制动作
使用此屏幕可配置Ranorex Studio在搜索UI元素时是仅评估一个应用程序，多个应用程序或所有正在运行的应用程序。这是Ranorex Studio的[👉白名单][10]功能的一部分。

1. 选择一个：

a. **focus on single application**                 
Ranorex Studio仅在您之前选择的测试应用程序中录制用户交互。其他一切都被忽略了。白名单仅包含您的AUT。

b. **focus on multiple applications**               
除了AUT之外，您还可以将其他流程添加到由Ranorex Studio录制的白名单中。

c. **No focus applied**                 
录制所有用户交互。白名单是空的。

2. 单击Continue。


## 终端窗口和教程面板
终端窗口会解释了当设置安装完成将会发生什么，即教程面板将出现并为您提供快速教程，指导您完成测试的第一步。

1. 阅读说明，然后单击“finish”以完成设置。
![](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/A30/A3040-0000051.png)

## 桌面解决方案及其项目的结构
完成设置后，Ranorex Studio将在测试套件视图中打开一个简单的预构建桌面测试套件。此测试套件是使用此桌面解决方案自动创建的测试套件项目的一部分。
![](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/A30/A3040-0000061.png)

1. 测试套件视图
您可以在此处构建和控制测试。

2. 您的解决方案附带一个包含简单预构建测试套件的项目。它包含一个带有三个录制模块的测试用例：StartAUT 它启动演示应用程序，  Recording1  为空并准备好录制测试动作，以及CloseAUT 关闭演示应用程序。

3. 录像模块视图
在Recording1的录像模块视图中，您可以录制和管理测试动作。

4. 空动作表
这是您录制的动作的显示位置。

>**章节预览**           
有关录制测试的更多信息，请参阅：               
Ranorex Studio基础> [👉Ranorex录制器][6]             
有关测试套件的更多信息，请参阅：            
Ranorex Studio基础> [👉测试套件][7]

## StartAUT和CloseAUT模块

桌面解决方案模板中的StartAUT和CloseAUT模块使用特殊机制来确保关闭已启动AUT的正确实例。这样可以提高基于模板的测试的稳定性。该机制基于变量和参数的高级概念，这就是为什么解决方案带有绑定到两个模块的变量的原因。

![](https://www.ranorex.com/rx-media/rx-user-guide/latest/A30/A3040-0000065.png)

**贴士**            
>您无需熟悉变量和参数即可使用桌面解决方案模板。

>**章节预览**              
如果要了解有关变量和参数的更多信息，请参阅           
Ranorex Studio高级>数据驱动测试> [👉定义变量][8]             
Ranorex Studio高级>数据驱动测试> [👉参数][9]


---
[👈示例项目][1]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
[创建一个新的测试项目👉][2]

[0]:https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/ranorex-studio/creating-new-test-project/

[1]:.\sample-projects.html
[2]:.\creating-new-test-project.html
[3]:.\web-mobile-testing\web-testing.html
[4]:.\web-mobile-testing\android-testing.html
[5]:.\web-mobile-testing\ios-testing.html
[6]:..\\..\\ranorex-studio-fundamentals/ranorex-recorder/introduction.html
[7]:..\\..\\ranorex-studio-fundamentals/test-suite/introduction.html
[8]:.\ranorex-studio-advanced\data-driven-testing\conditions-rules.html
[9]:.\ranorex-studio-advanced\data-driven-testing\parameters.html
[10]:..\\..\\ranorex-studio-fundamentals/whitelisting/whitelisting.md
[11]:..\\..\\ranorex-studio-fundamentals/ranorize-20-minutes/introduction.html