# [译] 执行数据驱动测试


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2018年9月17日-green.svg?longCache=true&style=flat-square)
![](https://img.shields.io/badge/UpdateTime-2019年9月29日-green.svg?longCache=true&style=flat-square)

---

**本章导视**

- [下载样本解决方案](#下载样本解决方案)
- [运行测试](#运行测试)
- [在运行时计算机上执行无MicrosoftExcel的测试](#在运行时计算机上执行无MicrosoftExcel的测试)



**视频向导**
>屏幕录像“运行数据驱动的测试”将带您了解本章中的信息。               
[立即观看](https://www.youtube.com/embed/e58NLP9See4)

## 下载样本解决方案
这是完整的示例解决方案，已经执行了前几章的所有说明并可以运行。

**示例解决方案**
>主题：运行数据驱动的测试            
时间：5分钟               
[立即下载](https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleDataDrivenTestingComplete.zip)


### **安装示例解决方案：**
1. 解压缩到计算机上的任何文件夹。

2. 启动 Ranorex Studio并打开解决方案文件RxDatabase.rxsln


**暗示**
>示例解决方案可用于Ranorex 8.0或更高版本。您必须同意8.2及更高版本的自动解决方案升级。

## 运行测试
1. 检查所有变量是否正确绑定。

2. 点击运行。

![B1050-0000010](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1050-0000010.png)


### **结果**
测试完成后，将显示报告。结果中显示了数据驱动的测试用例的行。

![B1050-0000020](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1050-0000020.png)


### **数据驱动测试的结果详细信息**

当我们对测试用例进行更详细的研究时，我们看到它对每个数据行都进行了一次迭代。因此，测试案例总共运行了8次。

每次迭代的详细信息还显示了该迭代的当前变量值。

![B1050-0000030](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1050-0000030.png)

>**章节预览**
>报告在Ranorex Studio基础知识> [👉报告][1]中进行了详细说明。

## 在运行时计算机上执行无Microsoft Excel的测试

如果要通过[👉XCOPY][2]或[👉Ranorex Agent][3]部署使用Excel连接器的数据驱动测试，则目标计算机不需要安装Excel许可证。只需在目标计算机上安装[Microsoft Access Database Engine Redistributable> = 2013](https://www.microsoft.com/en-us/download/details.aspx?id=54920)，即可运行测试。

您还可以在解决方案设置文件中配置不依赖Excel的执行实现的行为。

1. 在项目视图中，打开解决方案设置文件。

![B1050-0000040](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1050-0000040.png)

2. 找到设置<Testing.Data.ExcelDataLoadingPreference>。

3. 输入四个选项之一（所有图像都输入在图像中用于说明目的）：

a.PreferExcel：默认。如果可用，则使用Excel，否则使用AceOleDb（免费数据库引擎）。如果两个都不可用，则测试失败。

b.PreferAceOleDb：如果可用，使用AceOleDb，否则使用Excel。如果两个都不可用，则测试失败。

c.RequireExcel：仅使用Excel。如果不可用，则测试失败。

d.RequireAceOleDb：仅使用AceOleDb。如果不可用，则测试失败。

![B1050-0000050](https://www.ranorex.com/rx-media/rx-user-guide/v9.1/B10/B1050-0000050.png)




---

[👈数据绑定][4]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[参数👉][5]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/data-driven-testing/data-data-management/
[1]: ..\\..\\ranorex-studio-fundamentals\reporting\introduction.html
[2]:..\\..\\interfaces-connectivity/xcopy-deployment.html
[3]:..\\..\\ranorex-studio-fundamentals/ranorize-20-minutes/introduction.html
[4]:.\data-binding.html
[5]:.\parameters.html