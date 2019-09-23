# [译]详细的动作列表

*原文地址 👉 [Detailed list of actions][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2019-9-6*    

---
在本章中，您将找到所有动作的列表，其中包含有关其组件和属性的详细信息。可以在动作表中配置的所有组件也可在动作的属性中使用。我们将在本章中仅解释特定于动作的属性。该标准的特性在👉[管理动作][1]中得到解释。



**本章导视**
- [鼠标](#鼠标)
- [鼠标滚轮](#鼠标滚轮)
- [触摸](#触摸)
- [滑动手势](#滑动手势)
- [快捷键](#快捷键)
- [键序列](#键序列)
- [移动按键](#移动按键)
- [验证](#验证)
- [调用动作](#调用动作)
- [获取值](#获取值)
- [设定值](#设定值)
- [打开浏览器](#打开浏览器)
- [运行应用程序](#运行应用程序)
- [部署Android应用](#部署Android应用)
- [部署iOS应用程序](#部署iOS应用程序)
- [设置设备方向](#设置设备方向)
- [关闭应用](#关闭申请)
- [等待](#等待)
- [记录报告](#记录报告)
- [分隔器](#分隔器)
- [延迟](#延迟)
- [用户代码](#用户代码)


## 鼠标
摘要：执行鼠标动作。

类型：基本动作

是否可为变量:是

是否可以连接到控件库:是

### **描述**

按下鼠标上的按钮或将鼠标移动到指定位置。

### **组件**

子动作

- 向上/向下：向下按住并按住指定的鼠标按钮，向上按下它。
- 单击/双击
- 移动：将鼠标移动到指定的动作点。

### **按键**
指定按下哪个按钮。XButtons指的是鼠标上的侧面按钮。

### **动作点**
定义屏幕上按下按钮的位置或鼠标移动的位置。可以是相对位置，x; y像素坐标，或变量。

### **特定于动作的属性**
 - 禁用绑定警告：禁用报告中的“超出范围”警告。默认值为False。
 - 基于图像：配置参数👉[基于图像的自动化][2]。
 - 移动时间：鼠标移动动作需要多长时间。默认值为300毫秒。可以绑定到变量。


## 鼠标滚轮
 

摘要：执行鼠标滚轮动作

类型：基本动作

是否可为变量:是

是否可以连接到控件库:否


### **描述**

在垂直或水平方向上执行鼠标滚轮动作。

### **组件**

取向

水平垂直

三角洲
滚轮垂直或水平移动的距离为正整数或负整数。可以绑定到变量。

## 触摸
 

摘要：执行触摸屏动作

类型：基本动作

是否可为变量:否

是否可以连接到控件库:是，必需

### **描述**

触摸屏设备上的各种触摸滑动动作，必须链接到控件库项目。

### **组件**
触摸式
- 触摸
- 双击
- 长按
- 触摸开始/ 触摸移动 / 触摸结束

动作点

定义屏幕上将进行触摸动作的位置，或者对于TouchMove类型，定义移动位置。可以是相对位置，x; y像素坐标，或变量。

### **特定于动作的属性**
- 禁用绑定警告：禁用报告中的“超出范围”警告。默认值为False。
- 基于图像：配置参数👉[基于图像的自动化][2]。
- 触摸持续时间长：持久触摸多长时间。默认值为1秒。可以绑定到变量。
- 移动时间：触摸移动动作需要多长时间。默认值为100毫秒。可以绑定到变量。
- 触摸持续时间：触摸持续多长时间。默认值为100毫秒。可以绑定到变量。


## 滑动手势

摘要：	执行触摸屏滑动手势

类型：	基本动作

是否可为变量:	是

是否可以连接到控件库: 	是，必需

### **描述**
对特定控件库项执行滑动动作。您可以配置滑动的方向，距离和持续时间。

### **组件**
滑动方向

滑动方向的度数。可以设置为任何值或绑定到变量。

距离

滑动覆盖的距离（以像素为单位）。可以设置为任何值或绑定到变量。

滑动持续时间

滑动需要多长时间。可以设置为任何值或绑定到变量。

### **特定于动作的属性**
- 禁用绑定警告：禁用报告中的“超出范围”警告。默认值为False。
- 基于图像：配置参数👉[基于图像的自动化][2]。
- 开始位置：滑动开始的位置。默认为中心。各种预定义值。也可以是x; y像素值。可以绑定到变量。
- 步骤：滑动手势执行的次数。可以绑定到变量。

## 快捷键
摘要：	执行键盘快捷键
类型：	基本动作
是否可为变量：	是
是否可以连接到控件库: 	是

### **描述**
使用一个或多个键执行键盘快捷键。

### **组件**
键代码
- 按：按下并释放键盘快捷键。
- 向上，向下：按下并按住，向上释放键盘快捷键。

快捷键

键盘快捷键本身。单击该字段旁边的`...`以打开助理。您也可以直接输入快捷方式。例如，要执行复制快捷方式，请输入：ctrl+c并按Enter键。您还可以在动作属性中使用快捷方式配置程序，也可以是一个变量。

### **特定于动作的属性**
关键数据：执行的快捷方式。包含一个简单的快捷键配置器，包含所有可能的组合。可以绑定到变量。

按时间：按下后键盘快捷键保持多长时间。可以绑定到变量。

## **键序列**
摘要：	输入一个键序列

类型：	基本动作

是否可为变量:	是

是否可以连接到控件库: 	是

### **描述**
输入任意长度的键序列。您可以在动作的属性中屏蔽输入的序列。

### **组件**
**序列**

输入时的关键序列。单击该字段旁边的`...`以打开助理。

### **特定于动作的属性**
掩码序列：掩码输入的序列。默认值为False。

按时间：按下序列中的每个键多长时间。可以绑定到变量。

## **移动按键**
摘要：	按下移动键。

类型：	基本动作

是否可为变量:	是

是否可以连接到控件库: 	是，必需

### **描述**

按下移动动作键，例如Home或Back按钮。

### **组件**

**键**

要按的动作键。

### **特定于动作的属性**

基于图像：配置参数👉[基于图像的自动化][2]。

键：按下的动作键。可以绑定到变量。


## **验证**
摘要：	执行验证。

类型：	智能动作

是否可为变量:	是

是否可以连接到控件库: 	是，必需

### **描述**
对控件库项执行验证，即检查预期状态和实际状态是否匹配。根据结果​​，此动作将记录报告的成功或失败。可以使用几种不同类型的验证，每种验证都有自己的参数。

验证动作很复杂。不同的验证类型共享一组特定于动作的属性，但有些属性具有自己的附加属性。

### **共享验证属性**
动作：验证的类型。其余属性根据此属性而更改。

消息：将记录到报告以进行验证的消息。保留为空以使用默认的Ranorex消息。

失败时的报告级别]：失败消息👉[报告级别][3]。

成功报告级别：成功消息👉[报告级别][3]。

报告屏幕截图：报告消息中是否包含屏幕截图。

### **验证类型和特殊属性**
**存在**

检查控件库项是否存在。如果项目存在则记录成功，如果项目不存在则记录失败。

**不存在**

检查控件库项是否不存在。如果项目不存在则记录成功，如果项目不存在则记录失败。

AttributeEqual：

检查属性（列匹配名称）是否等于定义的值（列匹配值）。可用属性根据引用的控件库项而更改。同样，可能的匹配值也会根据属性而改变。例如，属性Text仅采用文本字符串，而属性Valid采用true / false值。匹配名称和匹配值都可以绑定到变量。

特殊属性：匹配名称和匹配值，如上所述。

AttributeNotEqual：

检查属性（列匹配名称）是否不等于定义的值（列匹配值）。可用属性根据引用的控件库项而更改。同样，可能的匹配值也会根据属性而改变。例如，属性Text仅采用文本字符串，而属性Valid采用true / false值。匹配名称和匹配值都可以绑定到变量。

特殊属性：匹配名称和匹配值，如上所述。

AttributeRegEx：

检查属性（列匹配名称）是否与定义的正则表达式匹配（列匹配值）。可用属性根据引用的控件库项而更改。匹配名称和匹配值都可以绑定到变量。

特殊属性：匹配名称和匹配值，如上所述。

AttributeContains

检查属性（列匹配名称）是否包含已定义的值（列匹配值）。可用属性根据引用的控件库项而更改。匹配名称和匹配值都可以绑定到变量。

特殊属性：匹配名称和匹配值，如上所述。

AttributeNotContains

检查属性（列匹配名称）是否不包含定义的值（列匹配值）。可用属性根据引用的控件库项而更改。匹配名称和匹配值都可以绑定到变量。

特殊属性：匹配名称和匹配值，如上所述。

ContainsImage

这是一个[基于图像的自动化][2]验证。执行验证时，它会创建控件库项目当前状态的屏幕截图。然后它检查此图像是否包含预定义的屏幕截图（列屏幕截图名称）。单击屏幕截图名称列中的...以打开一个对话框，以帮助您定义屏幕截图。

特殊属性：

基于图像：配置参数👉[基于图像的自动化][2]。

报告相似性：定义是否将两个图像的相似性记录到报告中。

CompareImage
这是一个[基于图像的自动化][2]验证。执行验证时，它会创建控件库项目当前状态的屏幕截图。然后它检查此图像是否与预定义的屏幕截图（列屏幕截图名称）相同。单击屏幕截图名称列中的`...`以打开一个对话框，以帮助您定义屏幕截图。

特殊属性：

基于图像：配置参数👉基于[图像的自动化][2]。

报告差异图像：定义是否将显示不同像素的差异掩码以及差异图像记录到报告中。

报告相似性：定义是否将两个图像的相似性记录到报告中。

>**章节预览**   
Ranorex Studio基础知识>测试验证>👉[简介][4]中介绍了测试验证的概念。

## **调用动作**
摘要：	调用一个动作

类型：	智能动作

是否可为变量:	是

是否可以连接到控件库: 	是，必需

### **描述**
直接调用引用的控件库项目上的特定动作，无需通过鼠标单击，按键等进行任何模拟的UI交互。特别适用于访问不可立即显示的UI元素，例如列表中的项目; 或窗口中没有焦点的下拉菜单或按钮。

### **组件**
**动作名称**

调用的动作。根据引用的控件库项进行更改。

**各种参数**

大多数动作不需要任何参数。但有些人会这样做。参数出现在动作名称后面的括号中，例如InvokeMethod（Name）。在动作表或属性中定义它们。它们可以绑定到变量。

>**章节预览**    
有关使用Invoke动作的示例，请参阅Ranorex Studio基础知识>动作>👉[调用动作][5]。


## **获取值**
 

摘要：	从控件库项属性中检索值。

类型：	智能动作

是否可为变量:	是

是否可以连接到控件库: 	是，必需
 

 

### **描述**
从控件库项属性中检索值并将其传递给变量。根据分配的控件库项目，可用属性会更改。在传递给变量之前，还可以使用RegEx修改检索到的值。

使用此动作的常见方案是检索特定交互结果的值。然后，将此值传递给在验证中使用的变量，该变量用于检查交互结果是否正确。

### **组件**

![A6050-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6050-0000010.png)     
*GetValue动作示例*

1. 将检索其值的**属性**。
2. 将检索到的值传递给**变量**。
3. **正则表达式**，在将值传递给变量之前将根据该正则表达式进行修改。
4. 引用的**控件库**项。

## **设定值**
摘要：	将存控件项的属性设置为定义的值。

类型：	智能动作

是否可为变量:	是

是否可以连接到控件库: 	是，必需

### **描述**
将控件库项属性设置为已定义的值。根据分配的控件库项目，可用属性会更改。该值也可以被屏蔽。

### **组件**

![A6050-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6050-0000020.png)     
*SetValue动作示例*

1. 将设置为已定义值的**属性**。
2. 属性将设置为的**值**。可以绑定到变量。
3. 引用的控件库项。
   
### **特定于动作的属性**

掩码值：掩盖值。默认值为False。


## **打开浏览器**
摘要：	打开浏览器并导航到指定的URL。

类型：	智能动作

是否可为变量:	是

是否可以连接到控件库: 	否

### **描述**
启动浏览器，对其进行检测并打开指定的网站。

### **组件**
![A6050-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6050-0000030.png)                   
*打开浏览器的动作*

1. 浏览器启动后将导航到的URL。可选的。可以绑定到变量。
2. 该浏览器启动。可以绑定到变量。
3. 浏览器窗口是否最大化。


### **特定于动作的属性**
参数：定义在启动浏览器时使用的命令行参数，例如-ProfileManager在打开概要文件管理器的情况下启动Firefox。可以绑定到变量。

清除缓存：启动时是否清除浏览器的缓存。 默认是假的。可以绑定到变量。

清除cookie：浏览器的cookie是否会在启动时被清除。 默认是假的。可以绑定到变量。

隐身模式：浏览器是否以隐身模式启动。 默认是假的。可以绑定到变量。

仪器：自动检测浏览器。通过XCOPY或Ranorex代理在运行时环境中部署测试时特别有用。默认为True。
关闭现有：以前打开的浏览器实例是否会在启动时关闭。 默认是假的。可以绑定到变量。

## **运行应用程序**
 

摘要：	从给定目录运行应用程序
类型：	智能动作
变量可能：	是
可链接到控件库：	否

### **描述**
直接从指定目录运行应用程序。

### **组件**

![A6050-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6050-0000040.png)      
*运行应用程序动作*

1. 应用程序的路径。如果应用程序与测试套件可执行文件位于同一文件夹中，则可以是相对的。可以绑定到变量。
2. 将运行应用程序的命令行参数。可能的参数取决于应用程序。可以绑定到变量。
3. 工作目录：
- 应用程序工作目录的可选信息
- 可以设置为常量值，也可以设置为变量
- 如果没有更改，则类似于应用程序可执行文件的目录

**特定于动作的属性**
- 返回值类型/变量：这两个字段用于处理“运行”应用程序动作的返回值。返回值始终是已执行应用程序的进程ID。因此，类型始终为System.Int32，即整数。返回值变量允许您选择要将进程ID传递到的变量。
- 运行标志：允许您设置NoElevation标志。此标志运行没有Windows管理员权限的应用程序，例如作为普通用户。可以绑定到变量。
- 运行最大化：应用程序是否将最大化运行。默认值为False。


## **运行移动应用**
摘要：	在移动设备上运行应用程序。

类型：	智能动作

变量可能：	是

可链接到控件库：	否

### **描述**
在移动设备上运行应用。

### **组件**

**端点**

将运行应用程序的端点（即移动设备）。可以绑定到变量。

**启动参数**

应用程序将运行的命令行参数。可能的参数取决于应用程序。可以绑定到变量。

**重启应用**

如果应用程序已在运行，请重新启动它。可以绑定到变量。

>**章节预览**      
从Web和移动测试>移动测试>👉[简介][6]开始详细解释移动测试。


## **部署Android应用**
摘要：	使用Android应用程序并将其部署到移动设备。

类型：	智能动作

变量可能：	是

可链接到控件库：	否

### **描述**
使用Android应用程序并将其部署到指定的移动设备。

### **组件**

**端点**

应用程序将部署到的端点（即移动设备）。可以绑定到变量。

**文件名**

用于检测和部署的应用程序的路径。可以绑定到变量。

###**特定于动作的属性**

- 仪器APK：是否在部署之前对应用程序进行检测。默认为True。可以绑定到变量。

- 仪表选项：定义各种仪表选项。

- 超时：在动作失败之前，检测和部署可能需要的最长时间。可以绑定到变量。


>**进一步阅读**   
从Web和移动测试>移动测试>👉[简介][6]开始详细解释移动测试。


## **部署iOS应用程序**

摘要：	仪器是iOS应用程序并将其部署到移动设备。

类型：	智能动作

变量可能：	是

可链接到控件库：	否

### **描述**
使用iOS应用程序并将其部署到指定的移动设备。

### **组件**
**端点**

应用程序将部署到的端点（即移动设备）。可以绑定到变量。

**App档案**
用于检测和部署的app存档的路径。可以绑定到变量。

**应用程序ID**
用于检测和部署的应用程序的应用程序ID。可以绑定到变量。

### **特定于动作的属性**

仪表设置：定义各种仪表设置。
 
 >**章节预览**   
从Web和移动测试>移动测试👉[简介][6]开始详细解释移动测试。

## **设置设备方向**

摘要：	设置控件库项目的移动设备的方向。

类型：	聪明的动作

变量可能：	是

可链接到控件库：	是，必需

### **描述**
设置指定控件库项的移动设备的方向。

### **组件**

**取向**    
设备将设置的方向。提供纵向和横向方向。横向左侧表示设备顶部向左旋转。反之亦然。可以绑定到变量。

>**章节预览**   
从Web和移动测试>移动测试> 👉[简介][6]开始详细解释移动测试  。

## **关闭申请**
摘要：	关闭应用程序或网站。

类型：	智能动作

变量可能：	是

可链接到控件库：	是，必需
 

### **描述**
关闭应用程序或网站。

此动作可用于关闭应用程序和网站。如果'Close Method'设置为'CloseWindow'或“CloseWindowByProcessID”，则尝试关闭应用程序。如果参数'宽限期'设置为大于0毫秒的值，则在“宽限期”之后，如果关闭应用程序失败，则该进程将被终止。如果'Close Method'设置为'KillProcess'，应用程序的进程将立即终止，并忽略宽限期。

### **组件**
![A6050-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/actions/A6050-0000050.png)    
*关闭申请动作*

1. 该close方法。CloseWindow和CloseWindowByProcessID尝试关闭窗口。如果失败，它将在宽限期后终止进程。  KillProcess忽略宽限期并立即终止进程。CloseWindowByProcessID与“运行”应用程序动作的ReturnValue属性一起使用。

2. 如果应用程序的正常关闭失败，则宽限期是Ranorex在终止进程之前将等待的时间。可以绑定到变量。
3. 将关闭其父应用程序的引用控件库项。
4. 
## **等待**
 

摘要：	等待指定的UI状态发生。

类型：	智能动作

变量可能：	是

可链接到控件库：	是，必需

### **描述**

等待直到在特定时间内达到定义的状态。有几种不同的等待类型可供选择。

**存在**
等待引用的存控件项存在于指定的超时（列Timeout）中。超时可以绑定到变量。

**不存在**
等待引用的控件库项在指定的超时（列超时）内停止存在。超时可以绑定到变量。

AttributeEqual
等待引用的控件库项的属性（列匹配名称）等于指定超时内的指定值（列匹配值）。匹配名称和匹配值可以绑定到变量。可用属性根据控件库项目而更改。如果值在超时内不匹配，则动作将失败。

在动作属性中配置超时（等待超时）。它可以绑定到变量。

AttributeNotEqual
等待引用的控件库的属性（列匹配名称）停止等于指定超时内的指定值（列匹配值）。匹配名称和匹配值可以绑定到变量。可用属性根据控件库项目而更改。如果值在超时内未停止匹配，则动作将失败。

在动作属性中配置超时（等待超时）。它可以绑定到变量。

AttributeContains
等待引用的控件库项的属性（列匹配名称）包含指定超时内的指定值（列匹配值）。匹配名称和匹配值可以绑定到变量。可用属性根据控件库项目而更改。如果属性在超时内不包含匹配值，则动作将失败。

在动作属性中配置超时（等待超时）。它可以绑定到变量。

AttributeNotContains
等待所引用的控件库项的属性（列匹配名称）停止包含指定超时内的指定值（列匹配值）。匹配名称和匹配值可以绑定到变量。可用属性根据控件库项目而更改。如果属性未在超时内停止包含匹配值，则动作将失败。

在动作属性中配置超时（等待超时）。它可以绑定到变量。

## **记录消息**
摘要：	将项目记录到报告中。

类型：	智能动作

变量可能：	是

可链接到控件库：	是

### **描述**

将消息记录到报告中，或捕获屏幕截图或Ranorex快照。

### **组件**
**子动作**

日志：将消息记录到报告中。

屏幕截图：捕获屏幕截图并将其添加到报告中。

快照：捕获Ranorex快照并将其添加到报告中。

**信息**

将出现在报告中的消息。也适用于截图/快照捕获。可以绑定到变量。

**水平**

记录项目的👉[报告级别][3]。

### **特定于动作的属性**
-  类别：定义项目在报告中显示的类别。默认为用户。



## **分隔器**
摘要：	在actions表的当前位置插入分隔线。

类型：	智能动作

变量可能：	否

可链接到控件库：	否


### **描述**
在actions表的当前位置插入分隔线。使用它可以直观地分离或分组相关的动作。您可以添加标题文本来描述分隔符。分隔符及其标题文本也将显示在报表中。此动作对测试执行本身没有影响。它纯粹是增加美感。

>**章节预览**   

Ranorex Studio基础知识>报告> 👉[基本报告特征和数据][7]中也说明了分隔符动作。

## **延迟**
摘要：	延迟执行下一个动作。

类型：	智能动作

变量可能：	是

可链接到控件库：	控件库

### **描述**
在指定的时间内延迟执行下一个动作。实质上，此动作会暂停测试执行一段时间（但AUT仍将正常运行）。时间值可以绑定到变量。延迟不受涡轮模式的影响。

## **用户代码**
摘要：	添加用户代码动作。

类型：	智能动作

变量可能：	是

可链接的控件库：	是

### **描述**
添加用户代码动作。您可以从用户代码库添加现有用户代码动作，也可以自己编写代码。

>章节预览
基础知识>动作>  👉[用户代码动作][8]中进行了说明。
Ranorex Studio专家>用户代码库> 👉简介中介绍了[用户代码库][9]。

---

[👈管理动作][10]&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[调用动作👉][5]









[0]:.\https://www.ranorex.com/help/latest/ranorex-studio-fundamentals/actions/detailed-list-actions/

[1]:.\managing-actions.html
[2]:.\ranorex-studio-advanced\image-based-automation\Introduction.html
[3]:.\reporting\concept-report-levels-2.html
[4]:.\test-validation\introduction.html
[5]:.\invoking-actions.html
[6]:.\web-mobile-testing\mobile-testing\introduction.html
[7]:.\reporting\basic-report-characteristics-data.html
[8]:.\user-code-actions.html
[9]:.\ranorex-studio-expert\user-code-library.html
[10]:.\managing-actions.html