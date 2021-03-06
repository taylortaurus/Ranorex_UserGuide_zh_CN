# [译] 通过模块边界传值

*原文地址 👉 [Passing values through module boundaries][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-18*    

---

值和变量在它们的模块中是局部的。这通常意味着在一个模块中定义的变量不能在其他模块之间共享。有时候，在其他模块之间共享值和变量的内容是有用的，或者是必要的。
这里介绍是如何做到这一点!

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [示例解决方案](#示例解决方案)
- [测试示例定义](#测试示例定义)
- [解决方案](#解决方案) 
- [元变量定义](#元变量定义)
- [目标变量定义](#目标变量定义) 
- [传输参数定义](#传输参数定义)
- [结果](#结果)

## 示例解决方案

通过模块边界传递变量值的解释基于一个示例说明，该示例下方下载。

**练习，我能做什么？** 
> 主题：通过模块边界传递变量  
> 时间：30min以内  
> 下载：[点我下载][1]  

**安装**

1. 解压项目目录到你的计算机任一文件夹
2. 使用RanorexStudi打开`PassVar.rxsln`解决方案  

**贴士**  
示例解决方案适用于Ranorex版本8.0或更高版本。你需要将解决方案自动升级同意到8.2及更高版本的。

## 测试示例定义  

假设一个测试用例，其中一个文本字符串(即名称)将插入到数据库表单的两个独立文本字段中。每个文本插入由一个单独的录制模块实现。示例应用了将值从一个模块传递到另一个模块的概念，而不是插入文本字符串两次。

![B2050-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/raw/master/VariablesAndParameters/B2050-0000010.png)  
*模块边界传值示例*  

1. **InsertFirstName**
    - 录制模块表示将第一个文本字符串插入到文本字段`First Name`中
    - 此文本字符串的值也将复制到第二个文本字段
    - 在当前示例中，文本字符串未`John`  

2. **InsertLastName**
    - 录制模块表示将第二个文本字符串插入到文本字段`Last Name`中
    - 此文本字符串的值应与第一个文本字符串中的值相同
3. **AddEntry**
    - 录制模块表示单击添加条目按钮 

### 结果

结果是，两个文本字段包含相同的文本字符串——从第一个文本字段复制的第二个文本字符串。

![B2050-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2050-0000020.png)  
*传递变量的测试示例结果*  

### 解决方案

解决方案基于变量的概念。每个录制模块中的变量将值从一个文本字段“携带”到另一个文本字段。而且因为变量是它们(录制)模块的本地变量，所以需要父测试容器的传输参数将变量链接在一起。让我们来看看这个概念。  

![B2050-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2050-0000090.png)  
*通过模块边界传递变量的概念*  

1. 变量`$varFirstName`在录制模块`InsertFirstName`中是用来复制文本字符串的值
2. 变量`$varLastName `在录制模块`InsertLastName`中是用来写文本字符串的值
3. 传递参数`transferFirst2LastName`将两个变量链接在一起，并允许将一个值从一个记录模块传递到另一个

## 元变量定义  

在第一步中，将定义源变量。这是将源文本字符串复制到目标(录制)模块的变量。在当前示例中，这是录制模块`InsertFirstName.rxrec`中的第一个名称的文本字符串。

![B2050-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2050-0000030.png)  
*InsertFirstName.rxrec录制模块*  

**要点须知** 
1. 动作#1表示单击文本字段，动作#2表示插入'John'作为文本值
2. `Get value`从文本字段收集文本值
3. 获取的值将会处理成一个文本值
4. 文本值将会本地保存在变量`$varFirstName`
5. 从控件库`FirstName`中引用的UI元素中检索文本值

### 结果

文本字符串“John”被收集并复制到变量`$varFirstName`中。

![B2050-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2050-0000050.png)  
*定义元变量*

## 目标变量定义

在第二步中，要定义目标变量。这个变量的内容被写入第二个文本字段。在当前示例中，这是在记录模块`InsertLastName.rxrec`中完成的。

![B2050-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2050-0000040.png)  
*InsertLastName.rxrec录制模块*  

**要点须知** 
1. 动作＃1表示单击文本字段
2. `Get value`从文本字段收集文本值
3. `Key sequence`处理将文本值写入文本字段
4. 要写入的值取自变量`$varLastName`
5. 文本值将写入存储库项`LastName`引用的UI元素中

### 结果

文本字符串“John”取自变量`$varLastName`，并写入控件库项`LastName`引用的文本字段中。

![B2050-0000052](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2050-0000052.png)  
*定义目标变量*  

## 传递参数定义

由于变量是其模块的局部变量，因此有必要定义一个传递参数，将两个变量“链接”在一起，并允许变量之间交换变量值。这个传输参数将在包含两个记录模块的父测试用例或智能文件夹中定义。

![B2050-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2050-0000060.png)  
*创建传输参数*  

1. 选择父测试容器(测试用例或智能文件夹)并打开上下文菜单
2. 单击`Data binding`  

    ![B2050-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2050-0000070.png)  
    *分配变量给参数*  
3. 创建有意义名称的传输参数
4. 打开模块变量的下拉列表，检查这两个变量是否链接到transfer参数
5. 单击OK结束参数定义

### 结果

现在，两个录制器模块变量都使用父容器传输参数链接在一起。

![B2050-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2050-0000080.png)  
*定义的传输参数*  

1. 录制模块`InsertFirstName`的源变量`$varFirstName`
2. 目标变量`$varLastName`录制模块`InsertLastName`
3. 传递参数`transferFirst2LastName`的父级测试用例
4. 测试套件显示两个变量都成功绑定到传输参数

## 结果

如果你运行前文准备好的解决方案，你将会有如下结果。文本字段`First name`的文本字符创自动插入到文本字段`Last name`，就像是用户交互完成。值的传递是通过变量和父类参数来完成的。

运行测试用例`PassValuesThroughModules`模块，你将看到下面显示的结果:

![B2050-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2050-0000100.gif)  


[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/variables-parameter/passing-values-module-boundaries/
[1]: https://www.ranorex.com/rx-media/rx-user-guide/v8.2/download/RxSamplePassValue.zip