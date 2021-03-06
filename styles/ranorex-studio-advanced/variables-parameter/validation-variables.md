# [译] 验证变量

*原文地址 👉 [Validation variables][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-15*    

---

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [验证类型](#验证类型)
- [验证匹配操作](#验证匹配操作)
- [创建名称匹配变量](#创建名称匹配变量)
- [使用变量替代匹配的值](#录制器变量管理)
- [默认匹配的值](#录制器变量管理)
- [创建基于图像验证变量](#录制器变量管理)
- [验证变量管理器](验证变量管理器)

## 验证类型

基本上，我们将验证类型分为基于文本或基于属性的验证和基于图像的验证。根据验证类型，变量定义是不同的。

![B2040-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/raw/master/VariablesAndParameters/B2040-0000010.png)  
*验证类型*  

1. 基于文本或是属性的验证示例
2. 基于图像验证示例

## 验证匹配操作

验证匹配操作符不能通过变量实现自动化。对于验证操作，匹配操作符的选择是固定的。

![B2040-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2040-0000020.png)  
*验证匹配操作*

## 创建匹配名称的变量

匹配的名称是基于文本和属性的验证操作的一部分。从可用属性列表中选择一个属性可以设置为变量。

![B2040-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2040-0000030.png)  
*创建匹配名称的变量*  

1. `匹配名称`（在当前示例中，匹配的是文本属性） 
2. 匹配名称选项可用的属性列表
3. 创建匹配名称选项的变量操作

## 使用变量替代匹配的值

匹配值是基于文本和属性的验证的一部分。通常，匹配值是一个常量值，与对应的UI元素(即控件库项)检索的值匹配。用变量替换匹配值与录制器变量的规范非常相似。

![B2040-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2040-0000040.png)  
*使用变量替代匹配的值*  

1. 选择验证动作，打开匹配值的下拉列表并点击`As new variable`
2. 分配变量一个有意义的名称并单击`OK`
3. 可以看到新建的匹配值变量`$intDBEntries`  

## 默认匹配值

最初设置的值(即已记录的)将自动预先设置为默认变量值。在我们的示例中，最初记录的文本值' 1 '因此被设置为默认值。默认值可以随意更改。

![B2040-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2040-0000050.png)  
*默认匹配值*  

**提示** 
> 如果变量没有绑定到任何数据，则应用默认值。因此，请谨慎地选择默认值。

## 创建基于图像的验证变量

创建基于图像的验证变量与控件库变量的规范非常相似。相应验证图像的任何可用属性都可以用于自动化目的。

![B2040-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2040-0000060.png)  
*创建基于图像的验证变量*  

1. 选择验证动作并打开上下文菜单
2. 点击`Make repository item variable`  

    ![B2040-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2040-0000070.png)  
    *控件库变量定义*  

3. 打开验证图像属性的下拉菜单，使用变量替换（当前示例中是`controlname `属性）  
4. 分配变量一个有意义的名称并单击`OK`
5. 在路径编辑器中点击`APPLY`来结束变量的指定

**t贴士**  
> 如果未启动测试应用程序，且验证图像不可见，则路径编辑器可能无法查找和识别验证图像。在这种情况下，Ranorex使用离线的、可能无效的RanoreXPath。因此，在定义验证变量之前，启动被测试的应用程序并使验证图像可见。

![B2040-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2040-0000100.png)  
*未使用/使用验证图像编辑路径*  

1. 路径编辑器无法找到和识别相应的验证图像
2. 路径编辑器成功找到并识别相应的验证图像


**章节预读**  
> 在[控件库变量][1]一文，中详细介绍和解释了控件库变量。  


### 结果

你可以在控件库中找到相应控件库项的RanoreXPath被新的控件库变量部分替换的结果。

![B2040-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2040-0000080.png)  
*基于图像的变量验证*  

1. 验证动作中的控件项链接到相应的控件库
2. 用`controlname`变量替换了部分RanoreXPath

## 验证变量管理器

验证变量管理类似于录制器变量和控件库变量的变量管理，本文将对此进行简要总结。


### 录制器变量管理

![B2040-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2040-0000110.png)  
*录制器变量管理*  

1. 选择并打开包含验证变量的录制模块
2. 单击录制器工具栏中的`Variables`按钮以打开变量编辑器

**提示**  
> 只有当前录制模块的变量才显示在变量编辑器里  

![B2040-0000120](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2040-0000120.png)  
*变量编辑器中验证录制器变量*  

1. 变量名对应的默认值
2. 变量编辑器工具栏 
    - 用来复制和粘贴的菜单
    - 直接新增变量按钮
    - 移除不在使用的变量（变量清理） 
    - 从当前录制模块中的控件库里拷贝一个变量（如果变量存在的话）
3. 变量提示
    -  `Variable in use`: 分配到动作中正在使用的变量
    -  `Variable in use from repository`: 显示录制模块里控件库中正在使用变量
    -  `Variable not in use`: 变量已被定义，但是没有分配到动作项中 

### 控件库变量管理器

通过单击控件库工具栏中的`Variables`按钮来管理控件库变量。

![B2040-0000130](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2040-0000130.png)  
*打开控件库变量管理器*  

1. 点击控件库工具条上的`Variables`  

**提示** 
> 所有当前控件库变量会显示在变量编辑器里

![B2040-0000140](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/VariablesAndParameters/B2040-0000140.png)  
*控件库变量编辑器*  

1. 有变量名和默认值的控件库变量列表
2. 控件库变量工具条
    - 用来复制和粘贴的菜单
    - 直接新增变量按钮
    - 移除不在使用的变量（变量清理）
3. 变量提示
    -  `Variable in use`: 正在使用的变量，例如，被分配到控件库项的变量
    -  `Variable not in use`: 变量已被定义，但是没有分配到控件库项  

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/variables-parameter/validation-variables/
