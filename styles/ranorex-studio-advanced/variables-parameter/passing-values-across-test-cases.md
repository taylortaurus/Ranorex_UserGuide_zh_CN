# [译] 通过测试用例传值

*原文地址 👉 [Passing values across test cases][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-18*    

---

本节的目的是展示如何将值从一个测试用例传递到另一个测试用例。该概念类似于通过模块边界传递值，并使用将在父测试容器（智能文件夹，测试用例，测试套件）中定义的参数。


**本章导视，章节内段落跳转推荐使用右上角的锚点！**
- [示例解决方案](#示例解决方案)
- [测试示例定义](#测试示例定义)
- [解决方案](#解决方案) 
- [元变量定义](#元变量定义)
- [目标变量定义](#目标变量定义) 
- [传输参数定义](#传输参数定义)
- [链接元变量到传输参数](#链接元变量到传输参数)
- [链接目标变量到传输参数](#链接目标变量到传输参数)
- [结果](#结果)


## 示例解决方案

对跨测试用例传递变量值的解释基于一个示例示例，该示例可作为示例解决方案下载。

**练习，我能做什么？** 
> 主题：通过测试用例传递变量  
> 时间：30min以内  
> 下载：[点我下载][1]  

**安装**

1. 解压项目目录到你的计算机任一文件夹
2. 使用RanorexStudi打开`PassVar.rxsln`解决方案  

**贴士**  
示例解决方案适用于Ranorex版本8.0或更高版本。你需要将解决方案自动升级同意到8.2及更高版本的。

## 测试示例定义

假设一个测试，其中插入到一个应用程序的文本字段中的文本字符串(即名称)需要重用，并插入到另一个应用程序的文本字段中。在Ranorex的一个测试套件中，源和目标文本字段在不同的测试用例中处理。

### 测试应用程序一

![B2060-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2060-0000010.png)    
*测试示例-部分1*  

1. 录制模块`InsertName`负责将文本字符串`Harry`插入第一个应用程序的文本字段
2. 录制模块`SubmitName`表示单击`Submit`按钮

### 测试应用程序二

3. 录制模块`SelectDatabase`表示对应用程序2的更改
4. 录制模块`CopyNameFromIntro`表示将从应用程序1复制的名称插入到文本字段`First name`中 

## 解决方案

每个文本插入在一个单独的测试用例中表示。两个测试用例都包含在同一个测试套件中，并且具有相同的父智能文件夹PassValuesThroughTestcases。该解决方案基于负责复制和粘贴相应模块中的文本值的局部变量。由于变量是测试容器的本地变量，因此有必要定义一个参数，该参数将变量链接在一起，从而支持跨不同测试用例的数据传输。  

![B2060-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2060-0000030.png)  
*通过测试用例传值--解决方案概览* 

1. 传输参数`transferValues`
    - 该参数在父智能文件夹`PassValuesThroughTestcases`中声明
    - 因此，所有子测试容器都可以访问它，即两个测试用例`InsertName`和`InsertFirstName2DB`
    - 此参数允许在测试用例之间传递值
2. 元变量`$varNameIntro`
    - 测试用例`InsertName` 的本地变量
    - 目的是把文本值复制到元文本字段
3. 目标变量`$varNameFromIntro`
    - 测试用例`InsertFirstName2DB` 的本地变量
    - 目的是把文本值粘贴到目标文本字段

## 元变量定义

在第一步中，将定义源变量。这是将源文本字符串复制到目标测试用例的变量。在当前示例中，这是录制模块`InsertName`中的名称的文本字符串。

![B2060-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2060-0000020.png)  
*InsertName.rxrec录制模块*  

**要点须知** 
1. 动作#1表示单击文本字段，动作#2表示插入'Harry'作为文本值
2. `Get value`从文本字段收集文本值
3. 获取的值将会处理成一个文本值
4. 文本值将会本地保存在变量`$varNameIntro`
5. 从控件库`EnterYourName`中引用的UI元素中检索文本值

### 结果

文本字符串“Harry”被收集并复制到变量`$varNameIntro`中

![B2060-0000031](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2060-0000031.png)  
*元变量定义*  


## 目标变量定义

在第二步中，要定义目标变量。这个变量的内容被写入目标文本字段。在当前示例中，这是在录制模块`InsertFirstName2DB.rxrec`中完成的。

![B2060-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2060-0000040.png)  
*InsertFirstName2DB.rxrec录制模块*  

**要点须知** 
1. 动作＃1表示单击文本字段
2. `Key sequence`处理将文本值写入文本字段
3. 要写入的值取自变量`$varNameFromIntro`
4. 文本值将写入存储库项`FirstName`引用的UI元素中

### 结果

文本字符串'Harry'取自变量`$varNameFromIntro`，并写入存储库项`FirstName`引用的文本字段。


![B2060-0000032](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2060-0000032.png)  
*定义目标变量*  

## 传输参数定义

由于变量是测试容器(测试用例、智能文件夹)的本地变量，因此有必要定义一个传递参数，将变量“链接”在一起，并允许变量之间交换变量值。这个传输参数将在包含两个测试用例的父测试用例或智能文件夹中定义。

![B2060-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2060-0000050.png)  
*创建传输参数*  

1. 选择父测试容器(测试用例或智能文件夹)并打开上下文菜单
2. 单击`Data binding` 

    ![B2060-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2060-0000060.png)  
    *传输参数声明*  
3. 创建一个新的传输参数并给它一个有意义的名称
4. 注意，参数不能链接到父测试容器中的变量。将模块变量绑定保持为空并单击OK

**提示**  
> 变量对它们的测试容器是私有的。因此，它们在自身所在的测试容器中以外是不可访问的。但参数可向下访问测试容器结构。因此，参数和变量之间的链接需要在变量的测试容器中完成。


## 链接元变量到传输参数

![B2060-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2060-0000070.png)  
*链接元变量到传输参数*

1. 选择有元变量录制模块的测试容器（测试用例）
2. 打开上下文菜单并单击`Data binding`

    ![B2060-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2060-0000080.png)  
    *元变量绑定数据*  
3. 查看传递参数`transferValues`的可访问性
4. 打开模块变量下拉菜单，选择源变量`$varNameIntro`进行绑定

### 结果

变量`$varNameIntro`绑定到传输参数`transferValues`

![B2060-0000034](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2060-0000034.png)  
*完成元变量定义*  

## 链接目标变量到传输参数  

![B2060-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2060-0000090.png)  
*链接目标变量到传输参数*  

1. 选择有目标变量录制模块的测试容器（测试用例）
2. 打开上下文菜单并单击`Data binding`

    ![B2060-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2060-0000100.png)  
    *目标变量绑定数据*  
3. 查看传递参数`transferValues`的可访问性
4. 打开模块变量下拉菜单，选择源变量`$varNameIntro`进行绑定 

### 结果

变量`$varNameIntro`绑定到传输参数`transferValues`

![B2060-0000035](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2060-0000035.png)  
*完成目标变量定义*  

## 结果

如果运行准备好的示例解决方案，你将看到插入到应用程序1的名称文本字段中的名称复制到应用程序2的名称文本字段中。

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/variables-parameter/passing-values-across-test-cases/
[1]: https://www.ranorex.com/rx-media/rx-user-guide/v8.2/download/RxSamplePassValue.zip
