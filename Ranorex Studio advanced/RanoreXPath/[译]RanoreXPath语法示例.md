# [译] RanorexXPath 语法示例

*原文地址 👉 [RanoreXPath syntax examples][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-7-9*  
*♋ update time : 2018-7-9*  

---

本章介绍了许多RanoreXPath语法示例，以加深您对在测试环境中应用强大的RanoreXPath规范的理解。  

## 测试示例定义

所有RanoreXPath解释示例都是使用Ranorex演示应用程序创建的。本文提供的大多数示例都是使用演示应用程序的**UI元素测试区域**完成的。  

![B6020-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000010.png) 
*Ranorex演示应用程序-UI元素测试区域*  

1. Ranorex 演示应用程序的UI元素测试区域  

### Ranorex演示应用程序  

可以按照以下显示的链接下载演示应用程序。 下载文件，解压缩并启动演示应用程序。  

> **下载**  
> 主题：Ranorex 演示应用程序  
> 时间：小于10min  
> [点我下载][1]

## 简单按钮识别  

本节介绍如何识别用户界面的简单按钮并分析相应的RanoreXPath规范。  

![B6020-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000020.png)  
*简单按钮识别*

1. 有关演示应用程序的 `退出` 按钮，请参阅RanoreXPath规范  
2. 树浏览器显示 `退出` 按钮是根UI元素 `RxMainFrame` 的直接子节点
3. 使用 `controlname` 识别 `退出` 按钮
4. Spy状态信息（左下角窗口）确认找到一个UI元素  

### RanoreXPath规范的一般化  

由于**退出**按钮是演示应用程序当前GUI层中的唯一按钮，因此可以概括RanoreXPath规范而不会丢失按钮的跟踪。如何做到请看下述。  

![B6020-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000030.png)  
*RanoreXPath规范的一般化*  

1. 请查看一般化的RanoreXPath规范，只使用了角色 `button` 和移除了谓词规范 
2. 树浏览器仍然将UI元素**退出**按钮显示为根元素的直接子元素  
3. 路径编辑器树视图显示了通用的RanoreXPath规范
4. 尽管如此，一个UI元素(即**退出**按钮)还是被标识出来了  

> **注意**  
> 此示例成功，因为在指定级别上只有一个按钮。如果添加了一个额外的按钮，当前示例将无法跟踪和标识一个按钮。  

## 用户定义的标识属性

Ranorex自动选择识别属性。 这个选择可以随意改变。 以下是如何选择用户定义的标识属性。  

![B6020-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000040.png)  
*用户定义的标识属性*  

1. 在路径编辑器中查看选择的属性值键值对 `controltext='Exit'`  
2. 谓词已添加到RanoreXPath规范中  
3. 它也显示在路径编辑的树视图中  
4. 结果，仍然会识别“退出”按钮  

> **提示**  
> Spy状态行显示RanoreXPath规范是否唯一，以及是否使用当前RanoreXPath规范标识了多少UI元素。  

## /？（任何可选的）通配符示例  

通配符为RanoreXPath规范增加了灵活性和健壮性。UI元素的识别对图形用户界面的结构变化更加具有抵抗力。目标是设计一个ui元素标识(理想情况下是独立于底层GUI结构的)。  

> **注意**  
> 记住前一节中的通配符定义:  
> 
> |通配符|含义|描述|
> |:--|:--:|:--|
>|`/*`|任意一个|任何UI元素，恰好是一（1）个树级别|
>|`/?`|任意一个可选|任何UI元素，正好是零（0）或一（1）树级别|
>|`//`|任意一个后代|任意数量的树级别的任何UI元素|  

![B6020-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000050.png)  
*'任何'通配符示例*  

1. 跟踪演示应用程序的UI元素测试区域的窗格  

### 结果

结果可以在Spy树浏览器和路径编辑器中看到。  

![B6020-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000060.png)  
*Spy树浏览器和'/？'示例的路径编辑器*  

1. **根**元素表示RanoreXPath规范的开头  
2. 中间的UI元素``TabPageList` 被两个 `/?` 通配符使路径规范健壮。即使 `TabPage` 元素向下或向上移动一级，该路径仍然有效  
3. **节点**UI元素是RanoreXPath规范的目标UI元素，并通过其角色和 `controlname` 属性定义  

### RanoreXPath解释:

![B6020-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000070.png)  
*RanoreXPath规范通配符/?示例*  

**目标元素**`3`是**根元素**`1`的后代元素，其中最多有两个（0,1或2）非必需指定的**UI元素**`2`  

## //（任何后代）通配符示例

通常需要在GUI中查找和跟踪元素，我们不知道元素的“**深度**”。因此，“所有路径后代”运算符允许搜索元素的“所有”后代级别以跟踪特定的UI元素。如何做到请看下述。  

![B6020-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000080.png)  
*使用//（任何后代）通配符的RanoreXPath规范示例*  

1. 参见演示应用程序程序窗口，它的角色 `/form` 指定为RanoreXPath规范的**根**元素  
2. 通配符运算符指定下面任何级别的任何元素  
3. 目标UI元素仅限于角色 `radiobutton`，即搜索根元素内和以下级别的任何单选按钮  

### 结果

结果可以在Ranorex Spy中看到。

![B6020-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000090.png)  
*//（任何后代）通配符的查找结果*  

4. 请参阅Spy的路径编辑器，其中RanoreXPath规范显示为树元素  
5. UI元素树浏览器显示所有找到的UI元素，即两个不同级别的7个单选按钮（级别3和级别4）  
6. Spy左下角的状态信息确认了7个找到的单选按钮

### RanoreXPath解释:

搜索并识别**根元素** `1`中和下级 `2`的**任一单选按钮** `3`。  

## / *(任何)通配符的例子  

如果要查找具有完全已知“深度”的UI元素，则可以使用“任何”通配符运算符作为您选择的工具。 请参阅其应用程序的简单示例。

![B6020-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000100.png)  
*具有/ *（任意）通配符的RanoreXPath规范*  

1. 演示应用程序的程序窗口作为RanoreXPath规范的**根**元素
2. 三个/*(任意)**通配符**操作符在根元素的下级三层搜索元素
3. 节点元素是角色为 `radiobutton` 的规范

### 结果

搜索和识别结果可以在Ranorex Spy中看到：

![B6020-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000110.png)  
*搜索结果为/ *（任意）通配符运算符*  

1. 请参阅具有树状结构的RanoreXPath规范元素的**路径编辑器**。每个通配符运算符代表根元素下面的一个搜索级别
2. 查看UI元素树浏览器，其中包含五（5）个角色 `radiobutton` 的UI元素，从根元素向下精确三（3）个级别  
3. 左下角状态行确认了5个找到的UI元素  

### RanoreXPath解释:

搜索并识别在**根元素** `1` 下方正好**三个等级** `2` 的**任何单选按钮** `3`  

## 缩小RanoreXPath规范  

在许多情况下，有必要将一般RanoreXPath规范缩小到更具体的规范，以便在GUI中查找和识别所选择的UI元素。这里介绍了缩小RanoreXPath规范的最常用方法。  

### 通用RanoreXPath规范   

让我们开始跟踪和识别演示应用程序的UI元素测试区域窗格中的所有按钮  

1. 启动Spy和演示应用程序并**指定**RanoreXPath，如下所示：

![B6020-0000120](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000120.png)  
*初始通用RanoreXPath规范的示例*  

1. 以树状形式查看具有RanoreXPath规范的所有元素的路径编辑器，搜索**UI元素测试区域**窗格中和下方的任何按钮  
2. 请在UI元素树浏览器查看，在演示应用程序中找到的17个按钮
3. 左下方的状态消息确认了17个找到的按钮  

### 缩小RanoreXPath规范 - 第一部分  

在第一步中，RanoreXPath规范被缩小到“可见”按钮，即在GUI中未隐藏的按钮。

1. 使用谓词更改RanoreXPath规范，如下所示：

![B6020-0000130](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000130.png)  
*缩小RanoreXPath规范的示例 - 第一部分*

1. 看到路径编辑器，其中节点元素使用属性 `visible ='True'` 进一步指定  
2. 看到UI元素树浏览器，其中包含基于当前RanoreXPath规范找到的15个结果按钮  
3. 左下方状态信息确认找到了15个按钮  

### 缩小RanoreXPath规范 - 第二部分

如果缩小RanoreXPath规范是不够的，则通过组合属性继续缩小，因为谓词可能是一种解决方案。查看下述这是怎么做的。  

1. 将下面列出的属性规范添加到当前RanoreXPath定义的谓词中。

![B6020-0000140](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000140.png)  
*缩小RanoreXPath规范的例子 - 第二部分*  

1. 看到缩小的**RanoreXPath**规范，并将第二个属性/值对作为谓词。  
    - 搜索设置为所有可见按钮...
    - 有一个以字母 `btn` 开头的**controlname**属性  
2. 看到UI元素树浏览器，其中包含两个与RanoreXPath搜索规范相关的UI元素  
3. 左下角的状态信息确认了两个找到的UI元素

> **提示**  
>  `>` 运算符是可以在RanoreXpath规范中使用的几个不同运算符之一。  


### 缩小结果:

缩小的RanoreXPath规范的搜索结果可以在下面显示的图像中看到 - “**UI元素测试区域**”窗格中的两个按钮被识别为匹配UI元素。  

![B6020-0000150](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000150.png)  
*缩小的RanoreXPath搜索结果示例*

## 在RanoreXPath规范中选择UI元素  

可以使用RanoreXPath语法的元素选择运算符直接选择一组跟踪和标识元素中的单个元素。下述介绍如何做到这一点。

1. 将下面列出的RanoreXPath规范**插入**到当前示例中  

![B6020-0000160](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000160.png)  
*在RanoreXPath规范中选择元素的示例*  

1. 看到**路径编辑器**，将选择 `[2]` 运算符添加到谓词中，从当前RanoreXPath规范标识的元素列表中选择第二个元素
2. 看到UI元素树浏览器，将第二个UI元素标识为RanoreXPath规范的搜索结果
3. 在左下角的Spy状态信息中看到搜索结果的确认  

### 选择结果：

选择结果是“**UI元素测试区域**”窗格的两个已识别按钮中的第二个：  

![B6020-0000170](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000170.png)  
*RanoreXPath选择结果*

> **提示**  
> 排序顺序就是UI元素在元素树中出现的顺序。该顺序是前面的谓词定义的结果，并且可能与UI元素命名没有任何共同之处（即“按钮1”）。  

## 树元素规范  

本节介绍和解释树元素的跟踪和识别。

![B6020-0000180](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000180.png)  
*使用Ranorex Spy跟踪树UI元素*  

1. 单击Ranorex Spy的Track按钮并跟踪
2. 演示应用程序中UI元素测试区域的树元素  

### 结果

Ranorex将树元素标识如下：

![B6020-0000190](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000190.png)  
*使用Ranorex识别树元素*  

1. 看到在网页和移动测试中树项目的追踪结果的RanoreXPath规范
2. Ranorex插入两个“任意可选”通配符（`/?/?`），为跟踪结果添加路径稳健性和灵活性
3. 网页和移动测试树项被识别为树的后代。如果树项在树的一个或两个级别之内和之下，则路径灵活性允许成功识别

### 子树项目规范

通过指定任何顶部节点的树节点来揭示在树内跟踪和识别树项的概念。

![B6020-0000200](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000200.png)  
*使用Ranorex Spy跟踪子树UI元素*  

1. 使用Ranorex Spy的**Track按钮**  
2. 跟踪演示应用程序的UI元素测试区域中的子树项目端点  

### 结果：

Ranorex识别子树项目如下：  

![B6020-0000210](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000210.png)  
*使用Ranorex Spy识别子树元素*  

1. 看到的RanoreXPath规范，并将子树项Endpoints标识为普通树项
2. Ranorex将树保留为RanoreXPath规范的祖先元素
3. 所有子树项都被标识为简单树项，通过**任何后代**通配符运算符独立于它们在树中的位置
4. 看到子树项被标识为规则树项，以及使用 `accessiblename` 作为谓词  

> **注意**  
> Ranorex将所有子树项视为常规树项，并通过唯一谓词规范来标识它们。树中的位置并不重要，因此，树结构的变化不会改变识别成功。  

### 树的兄弟姐妹的规格  

通过轴说明符对RanoreXPath规范进行简单修改，可以跟踪和识别当前树项的下一个和前一个兄弟树项。

![B6020-0000220](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000220.png)  
*将轴说明符应用于RanoreXPath规范*  

1. 看到RanoreXPath规范，添加的**轴说明符**跟踪以下树项同级
2. **路径编辑器**以树状结构显示RanroeXPath规范  
3. UI元素树浏览器显示标识结果，移动测试树项作为端点树项的下一个兄弟树项  

![B6020-0000230](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000230.png)  
*识别兄弟树项目*  

4. 查看正在测试的应用程序的**UI元素测试区域**，其中树元素移动测试显示为端点树项目的兄弟元素  

> **注意**  
> 如果存在多个兄弟元素，则轴指定符号 `follow -sibling` 返回所有后级的兄弟元素。。

## 表项目规范  

跟踪和识别表中的元素是一种高级规范方法，并且需要一些在此引入和解释的基本知识。  

### 基本表格方向

表格单元的寻址遵循一个重要的理解系统，并在下图中显示。  

![B6020-0000240](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000240.png)  
*基本表格方向*  

**重点：**

- 表列由其标题名称标识
- 表行已编号，在标题下方的第一行中以“0”开头
- 表格单元格通常由列名称和行号组合标识

1. 绝对单元格规范的示例：单元格“Thomas”由列名和行号组合绝对指定
2. 相对单元格规范的示例：单元格“Development”被相对指定为通过一个轴说明符 `/..`绝对指定一个锚单元格之后的第6个单元格。  

### 测试定义

当前测试示例的目的是在演示应用程序的UI元素测试区域的表中唯一地标识名为Thomas Bach的人的年龄。  

![B6020-0000250](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000250.png)  
*表格单元规范 - 测试定义*  

1. 看到**表格条目（行）**，其中包含名字，姓氏，年龄，性别和部门从属关系  
2. 托马斯巴赫的**年龄**将通过RanoreXPath规范强有力地选择  

### 绝对单元格位置规范  

在第一个简单的方法中，具有'Thomas Bach'人名的单元格可以通过单元格绝对位置来识别：  

![B6020-0000260](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000260.png)  
*绝对表格单元规范*  

1. 看到使用表单元格绝对指定的RanoreXPath规范
2. RanoreXPath规范引用“FirstName”列中的单元格和行号3 - 在我们当前的例子中 - 包含托马斯这个名字  
3. 看到Spy的树形浏览器视图中标识的UI元素  

### 缺少对表格单元格更改的稳健性  

绝对单元规范缺乏对表格单元布置的改变的鲁棒性。  

![B6020-0000270](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000270.png)  
*表单元格移动*  

1. 移动表格单元的排列显示...  
2. 绝对单元格导致错误的结果，因为规范依赖于单元格位置而不是期望的单元格内容  

### 单元格内容规格  

单元格位置规格的改进是单元格内容的规范，其中我们基于其内容识别单元格  

![B6020-0000280](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000280.png)  
*单元格内容规范*  

1. 指定单元格内容可以增强对表重组的稳健性，但是...
2. 导致识别具有指定内容的所有单元格，与列无关  

### 缩小范围的单元格规范  

还需要将单元格规范限制为名字'Thomas'（和姓氏'Bach'）。这是通过缩小的单元规范来完成的。

![B6020-0000290](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000290.png)  
*缩小范围的单元格规范*  

1. 看到缩小的单元格规范，其中两个属性构成RanoreXPath谓词...
2. 结果，是当前示例的唯一标识的单元格

> **提示**  
> 可能有必要通过附加属性和/或其他轴指定符进一步指定单元格，以便唯一地指定定义的单元格。在当前示例中，两个属性就足够了。  

### 相对单元格位置规范 

最后，为了指定名为“Thomas Bach”的人的年龄的单元格，需要相对单元格规范。

![B6020-0000300](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanoreXPath/B6020-0000300.png)  
*相对单元格规范*  

1. 使用单元格的accessname属性“Age”来相对指定识别单元格
2. 表中行为“Thomas Bach”的年龄为42

[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/ranorexpath/ranorexpath-syntax-examples/ 
[1]: https://www.ranorex.com/rx-media/rx-user-guide/v8.2/download/RxDemoApp.zip