# [译] 映射动态UI元素

*原文地址 👉 [Mapping dynamic UI elements][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-7-8*    
*♋ update time : 2018-7-10*  

---  

如果软件是基于动态内容的，那么它通常是基于动态标识符的。
这可能会导致对象识别方面的问题，因为每次显示一个元素时都会新生成这些标识符。
克服这一挑战的一种方法是在记录测试场景之后手动调整存储库，这当然非常耗时。
处理动态内容的推荐方法是使用RanoreXPath权重规则来优化特定动态框架的对象识别。  

## 什么是RanoreXPath权重规则？  

路径权值规则为满足一组已定义条件的特定功能设置特定属性的权值。权重将被用于构建RanoreXPath。高权重和且值不为空的属性用来标识UI元素。  

RanoreXPath权重规则可以通过“RanoreXPath权重规则”编辑器(Settings -> Advanced -> Edit Path Weights’ or ‘Ranorex Spy -> Edit Path Weights’)访问。  

![C1010-0000010-old](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudioExpert/C1010-0000010-old.png)  
*通过设置对话框编辑RanoreXPath权重规则*

![C1010-0000020-old](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudioExpert/C1010-0000020-old.png)  
*通过Ranorex Spy编辑RanoreXPath权重规则*

使用RanoreXPath权重规则可以帮助您自动创建健壮的存储库，这是健壮的测试自动化框架的基础。  


## 如何添加你自己的RanoreXPath权重规则

你可以在博文[自动化测试和动态ID][1]中找到如何添加你自己的RanoreXPath权重规则的详细说明。

如果你想在Ranorex社区分享你的RanoreXPath权重规则，请将你的XML规则发送至[support@ranorex.com][2]并提供简要说明。

## 如何添加共享的RanorexXPath权重规则

从设置对话框打开“RanorexXPath权重规则”编辑器(Settings -> Advanced -> Edit Path Weights)。

复制下面的某个XML规则（<**CTRL**> + <**A**>, <**CTRL**> + <**C**>），通过按<**CTRL**> + <**V**>或使用上下文菜单将其粘贴到'RanoreXPath权重规则'对话框。  

![C1010-0000030-old](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudioExpert/C1010-0000030-old.png)  
*添加共享的规则*

## 规则库

- RxWinForms ControlNet11 Classnames

```xml
<rule  
name="RxWinForms ControlNet11 Classnames"  
enabled="True"  
capability="nativewindow"  
attribute="class"  
setweight="0"  
conditionsoperator="and">  
    <condition  
    source="self"  
    attribute="class"  
    match="^WindowsForms10.Window"  
    negate="False"/>  
</rule> 
```

- RxWeb YUI (Yahoo User Interface Library)

```xml
<rule  
name="RxWeb YUI (Yahoo User Interface Library)"  
enabled="True"  
capability="webelement"  
attribute="id"  
setweight="0"  
conditionsoperator="or">  
    <condition  
    source="self"  
    attribute="id"  
    match="^yui(_\d+)"  
    negate="False"/>  
    <condition  
    source="self"  
    attribute="id"  
    match="^yui-gen.*"  
    negate="False"/>  
</rule> 
```

- RxWeb JS Frameworks (ExtJS, Sencha, Ozone Widget ,...)

```xml
<rule  
name="RxWeb JS Frameworks (ExtJS, Sencha, Ozone Widget ,...)"  
enabled="True"  
capability="webelement"  
attribute="id"  
setweight="0"  
conditionsoperator="or">  
    <condition  
    source="self"  
    attribute="id"  
    match="^ext-.*\d+.*"  
    negate="False"/>  
    <condition  
    source="self"  
    attribute="id"  
    match="^[a-z]+-\d{4}(-[a-z]*(-\d*)?)?"  
    negate="False"/>  
</rule> 
```

- RxWeb jQuery

```xml
<rule  
name="RxWeb jQuery"  
enabled="True"  
capability="webelement"  
attribute="id"  
setweight="0"  
conditionsoperator="or">  
    <condition  
    source="self"  
    attribute="id"  
    match="^ui-id-\d+"  
    negate="False"/>  
</rule> 
```

- RxWeb ASP.net

```xml
<rule  
name="RxWeb ASP.net"  
enabled="False"  
capability="webelement"  
attribute="id"  
setweight="0"  
conditionsoperator="or">  
    <condition  
    source="self"  
    attribute="id"  
    match="^ctl00(\$|_)(.*(\$|_))"  
    negate="False"/>  
</rule>
```

- RxWeb GWT

```xml
<rule  
name="RxWeb GWT"  
enabled="True"  
capability="webelement"  
attribute="id"  
setweight="0"  
conditionsoperator="or">  
    <condition  
    source="self"  
    attribute="id"  
    match="^gwt-uid-\d+.*"  
    negate="False"/>  
    <condition  
    source="self"  
    attribute="id"  
    match="^isc_.+"  
    negate="False"/>  
</rule>
```

- RxWeb MS Dynamics CRM

```xml
<rule  
name="RxWeb MS Dynamics CRM"  
enabled="True"  
capability="webelement"  
attribute="id"  
setweight="0"  
conditionsoperator="or">  
    <condition  
    source="self"  
    attribute="id"  
    match="[a-zA-Z_]+_{([0-9 A-F]+(-)?)+}_\d+"  
    negate="False"/>  
</rule>
```

- RxWin32 Random Control IDs

```xml
<rule  
name="RxWin32 Random ControlIds"  
enabled="False"  
capability="nativewindow"  
attribute="controlid"  
setweight="0"  
conditionsoperator="or"/>
```  



[0]: https://www.ranorex.com/help/latest/ranorex-studio-expert/mapping-dynamic-ui-elements/

