# [译] 将现有报告转换为PDF
    

[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月10日-green.svg?longCache=true&style=flat-square)

---

本文介绍如何使用ReportToPDF工具将现有Ranorex报告文件转换为PDF。这将允许您与未安装Ranorex的人共享报告。

**提示**  
> 如果您希望Ranorex在测试执行期间生成报表时将其转换为PDF，请使用`Ranorex Automation Helpers`中包含的`ReportToPDFModule`。

**本章导视**

- [下载报告转PDF工具](#下载报告转PDF工具)
- [转换现有的一个报告](#转换现有的一个报告)

>**视频向导**           
视频“转换报告”将引导您完成本章中的信息。              
[立即观看](https://www.youtube.com/embed/XFUGey_NgXU)


## 下载报告转PDF工具

ReportToPDF工具作为独立的可执行文件进行提供：

- Ranorex_PDF_Executable.zip: 用于转换现有报告文件的可执行文件(*.rxzlog)
- style.zip:生成PDF的样式表

## 转换现有的一个报告

ReportToPDF可执行文件是一个命令行工具，允许您将现有Ranorex报告转换为PDF。报告必须以压缩形式传递给转换器，即所谓的rxzlog。rxzlog是单个存档（.rxzlog扩展名），包括报告和所有相关文件。

使用以下调用从命令行执行ReportToPDF工具：

```bash
ReportToPDF.exe [input file] [output file] /[argument]
```

输入和输出文件是必需的，参数是可选的。

`[input]`:设为需要转换的文件
`[output]`:设为PDF名

### 允许的参数

`style`: 设置一个自定义样式表

`detail`: 指定生成的PDF中显示的信息量:
- `none`: 不显示任何模块动作
- `failed`: 仅显示故障模块的动作
- `all`: 所有的动作都显示（默认值）

---

[👈复杂的报告定制][1]

[0]: https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/reporting/converting-reports-data-types/
[1]: .\user-defined-reporting.html