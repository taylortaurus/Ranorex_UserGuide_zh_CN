# [译] 参数


[![](https://img.shields.io/badge/OfficialPage-ClickMe-blue.svg?longCache=true&style=flat-square)][0]  

[![](https://img.shields.io/badge/Translator-TaylorTaurus-42B983.svg?longCache=true&style=flat-square)](https://github.com/taylortaurus) 
![](https://img.shields.io/badge/TranslateTime-2019年9月29日-green.svg?longCache=true&style=flat-square)

---


在本章中，您将学习什么是参数，如何添加它们以及可以使用它们。

可以将参数视为只有一行的数据源，即最简单的一种数据源。它们对于保持模块可重用和测试可维护性很有用。它们还允许您将变量值从一个记录模块传递到另一个。


**本章导视**

- [添加参数](#添加参数)
- [使用参数](#使用参数)
- [示例1：提高模块的可重用性](#示例1：提高模块的可重用性)
- [示例2：在测试执行期间跨模块传递值](#示例2：在测试执行期间跨模块传递值)

**视频向导**
>视频“参数”将带您了解本章中的信息。           
[立即观看](https://www.youtube.com/embed/GoYbOeXh-MU)

## 添加参数
在项目的“ 属性”对话框的测试套件视图中添加参数。您可以将参数添加到：

- 测试套件项目（=全局参数）
- 测试容器（=本地参数）

**注意**
>将参数添加到项目时，其所有后代都将继承它。
>- 对于测试套件项目，这意味着所有测试容器都将继承它。
>- 对于测试容器，这意味着后代测试容器将继承它，而不继承其兄弟姐妹或父代。

### **参数对话框**
要访问添加参数对话框：

1. 右键单击要向其添加参数的项目，然后…

a.…对于测试套件，请单击Global parameters…。

b.…对于测试容器，单击数据绑定…。

![B1070-0000010](https://www.ranorex.com/rx-media/rx-user-guide/latest/B10/B1070-0000010.png)

![B1070-0000020](https://www.ranorex.com/rx-media/rx-user-guide/latest/B10/B1070-0000020.png)


1. 您添加的参数数量。没有限制。

2. 每个现有参数的名称。单击添加行…以输入新参数的名称。

3. 每个参数的默认值。为新参数分配一个值。任何字符串都是可能的。

4. 每个参数的当前绑定。使用下拉菜单将新参数绑定到一个或多个变量。

5. 斜体字的参数已从祖先继承。只能在祖先中编辑它们。

6. 单击自动创建可为任何未绑定变量自动创建参数。新参数的名称与未绑定变量的名称相同。然后单击“ 自动绑定”以将新参数自动绑定到各个变量。

## 使用参数
在本节中，我们将向您展示两个如何使用参数的示例。

第一个示例很简单，对于多种测试都非常有用。它与使用参数来提高记录模块的可重用性有关。

第二个例子是更复杂的，并在其应用程序的更多的限制，但仍非常有用的。它涉及在测试执行期间使用参数将值从一个变量传递到另一个记录模块中的另一个变量。这样可以提高效率并减少测试维护。

## 示例1：提高模块的可重用性

**注意**
>这个示例很短，因此没有专用的示例解决方案。

考虑一个提供不同功能的典型AUT。它将这些功能显示在用户通过UI访问的不同屏幕上。

例如，Ranorex Studio演示应用程序中有几个选项卡，每个选项卡提供不同的功能：

![B1070-0000030](https://www.ranorex.com/rx-media/rx-user-guide/latest/B10/B1070-0000030.png)


要测试这些屏幕，您需要创建几个不同的测试用例，每个屏幕一个。为什么？因为您要在每个屏幕上测试不同的功能，所以每种情况下的测试步骤都会有所不同。但是，第一步始终保持不变：打开AUT并弹出屏幕。它始终包含以下操作：

1. 打开AUT。
2. 单击要显示的屏幕的选项卡。

这使得模块具有高度可重用性，而可重用模块可提高效率。但是有一个问题：在每个测试用例中，要单击的选项卡的名称都不同。

解决此问题的最简单，最有效的方法是使用变量和参数。

### **定义一个变量**
在记录模块StartAUT中，我们将使存储库项目链接到Click操作变量。

1. 在演示应用程序的选项卡上定义鼠标单击操作，然后按照[👉定义变量][1]中有关存储库变量的说明进行操作。将变量命名为$ varTab。

![B1070-0000040](https://www.ranorex.com/rx-media/rx-user-guide/latest/B10/B1070-0000040.png)

### **定义参数和链接变量**
现在，我们将在第一个测试用例（Introduction_testing）中定义一个参数，并将存储库变量绑定到该参数。

1. 右键单击测试用例，然后单击数据绑定…。

2. 在“ 参数”下，为参数Tab 命名，并为其分配值Introduction。

**注意**
>参数值是RanoreXPath中标识UI元素的属性值。对于“简介”标签，该名称为[@ accessiblename =' 简介 ']。对于“测试数据库”选项卡，它将为[@ accessiblename =' 测试数据库 ']。              
有关更多信息，请转到Ranorex Studio高级> [👉RanoreXPath][2]

3. 将其绑定到变量varTab，然后单击“确定”。

![B1070-0000050](https://www.ranorex.com/rx-media/rx-user-guide/latest/B10/B1070-0000050.png)


4. 对其他测试用例重复此操作，并将参数值替换为标识相应选项卡的属性值，即测试数据库，基于图像的自动化等。

就是这样。运行测试时，它将自动通过选项卡。

## 示例2：在测试执行期间跨模块传递值
在此示例中，我们将向您展示如何在测试执行期间获取在一个模块中生成的值，并将其传递给同一测试运行中的另一个模块。我们将使用变量，参数和“获取值”操作来完成此操作。

为了解释这一点，我们将在Ranorex Studio演示应用程序中使用一个小型数据库测试。

### **下载样本解决方案**
由于此示例更加复杂，因此我们为您创建了示例解决方案。下载以下文件以按照说明进行操作。本节末尾提供了完成的样本。

**示例解决方案**
>主题：参数–在模块之间传递值                
时间：15分钟         
[立即下载](https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleParameter.zip)


安装示例解决方案：

1. 解压缩到计算机上的任何文件夹。

2. 启动 Ranorex Studio并打开解决方案文件。

### **测试说明**
在示例测试中，我们将使用数据驱动的测试将大量人员输入Ranorex Studio演示应用程序的数据库。对于每个条目，显示条目数量的计数器将增加。在测试运行结束时，我们希望将条目总数记录到报告中。

![B1070-0000060](https://www.ranorex.com/rx-media/rx-user-guide/latest/B10/B1070-0000060.png)

### **初始测试套件**

![B1070-0000070](https://www.ranorex.com/rx-media/rx-user-guide/latest/B10/B1070-0000070.png)

1. 启动演示应用程序，然后单击数据库注册。

2. 如前面的子章节所述，前六个记录模块将来自数据源的条目添加到数据库中。

3. 记录模块GetDBCounter将提取计数器值并将其写入变量。

4. 记录模块WriteMaxCounterToReport将计数器值记录到报告中。

5. 关闭AUT。

计数器值是在测试执行期间动态生成的 ，具体取决于添加的条目数量。例如，取决于数据源的更改或条件的包含，最终数量将有所不同。因此，我们无法可靠地知道测试执行期间的计数器值，否则每次查找都将花费大量的精力。要将正确的值自动记录到报告中，我们将需要使用变量和参数。

 

### **提取值并将其写入新变量**

首先，在测试执行期间添加所有条目之后，我们将使用“获取值”操作提取计数器值，并将其写入新变量：

1. 打开记录模块GetDBCounter。

2. 添加链接到条目计数器的存储库项目的“获取价值”操作。

3. 创建新变量$ varCounter。计数器的值将被写入该变量。

![B1070-0000080](https://www.ranorex.com/rx-media/rx-user-guide/latest/B10/B1070-0000080.png)

### **记录计数器值以进行报告**
现在，我们将添加操作以将计数器值记录到报告中。

1. 打开记录模块WriteMaxCounterToReport。

2. 如下图所示，添加两个新的日志消息操作。

3. 添加新变量$ varWriteCounter。该变量将从GetDBCounter模块接收值并将其记录到报告中。

![B1070-0000090](https://www.ranorex.com/rx-media/rx-user-guide/latest/B10/B1070-0000090.png)

### **创建传输参数**
在测试运行期间，GetDBCounter中的变量现在将接收动态生成的计数器值。但是，WriteMaxCounterToReport中的变量尚无法检索该值，因为变量及其值在其模块本地。我们需要“链接”变量。为此，我们将它们全部绑定到同一参数。

链接变量的参数必须位于两个模块的共同祖先中。在我们的例子中，模块位于两个单独的测试容器中，因此第一个共同祖先是测试套件项RxSampleParameter。如果两个模块位于同一测试容器中，则可以在其中添加参数。

1. 右键单击测试套件项目RxSampleParameter，然后单击全局参数…。

2. 在“ 参数”下，添加一个名为parCounter的参数。

3. 单击确定。

![B1070-0000100](https://www.ranorex.com/rx-media/rx-user-guide/latest/B10/B1070-0000100.png)


**注意**
>我们将该值保留为空以表明这是一个在测试执行期间接收其值的参数。您可以输入任何内容；该值将替换为测试运行。

### **将变量链接到参数**
添加参数后，我们现在可以将变量绑定到该参数并将它们链接在一起。这样，动态生成的值将从一个模块传递到另一个模块。

1. 右键单击测试用例AddPersonToDB，然后单击数据绑定…。

2. 在“ 参数”下，将继承的参数以斜体形式绑定到变量$ varCounter。

3. 单击确定。

![B1070-0000110](https://www.ranorex.com/rx-media/rx-user-guide/latest/B10/B1070-0000110.png)

在另一个测试用例中，对第二个变量重复该过程：

1. 右键单击测试用例WriteReport，然后单击数据绑定…。

2. 在“ 参数”下，将继承的参数以斜体形式绑定到变量$ varWriteCounter。

3. 单击确定。

![B1070-0000120](https://www.ranorex.com/rx-media/rx-user-guide/latest/B10/B1070-0000120.png)

这样，只要所有模块都可以访问相同的参数，就可以将值从一个模块传递到另一个模块中的另一个模块。自然地，这也仅按时间顺序工作，即，给定模块需要在接收模块之前执行。

运行测试后，您将看到计数器值已正确记录到报告中：

![B1070-0000130](https://www.ranorex.com/rx-media/rx-user-guide/latest/B10/B1070-0000130.png)


**示例解决方案**
>主题：参数–在模块之间传递值               
时间：15分钟       
[立即下载](https://www.ranorex.com/rx-media/rx-user-guide/latest/download/RxSampleParameterComplete.zip)


### **网络测试示例**
提取和传递动态生成的值在Web测试中也很重要。Ranorex Studio中包含的Web测试示例（Ranorex Studio起始页>示例解决方案> Web示例）演示了以下内容：

![B1070-0000140](https://www.ranorex.com/rx-media/rx-user-guide/latest/B10/B1070-0000140.png)


PublishNewPost模块输入帖子标题和内容，然后单击WordPress中的“发布”按钮。当您在WordPress中发布帖子时，它会自动为发布的帖子生成一个唯一的URL。

ValidatePost模块中需要此URL ，因此测试可以导航到博客文章并查看其是否正确发布。DeletePost模块中也需要它，以导航到要删除的正确帖子。

但是，与演示应用程序中的计数器值一样，我们不知道测试运行期间的URL。

因此，模块GetPostURL提取值，将其写入变量，然后将其传递给其他两个模块。除上面的示例中，所有模块都包含在同一测试用例中之外，其工作方式与上一个示例中说明的相同。因此，链接参数位于该测试用例中，并且所有变量都已绑定到该测试用例。



---

[👈执行数据驱动的测试][3]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[条件👉][4]

[0]:https://www.ranorex.com/help/latest/ranorex-studio-advanced/data-driven-testing/parameters/
[1]:.\preparations-data-driven-testing.html
[2]:..\\..\\ranorex-studio-advanced/ranorexpath/introduction.html
[3]:.\executing-data-driven-tests.html
[4]:.\conditions-rules.html