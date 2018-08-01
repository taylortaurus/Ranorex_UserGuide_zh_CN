# [译] RanoreXPath 中的正则表达式

*原文地址 👉 [Regular expressions in RanoreXPath][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-7-8*    
*♋ update time : 2018-7-10*  

---  

正则表达式regex或regexp(有时称为rational表达式)在理论计算机科学和形式语言理论中是定义搜索模式的字符序列。
通常，这种模式被计算机软件中的字符串搜索算法用于字符串的“查找”或“查找和替换”操作。
Ranorex也使用这种语法表达式来匹配RanoreXPath定义。  

有关正则表达式更全面的文档，请参阅相应的MSDN网站 👉 [.NET 正则表达式][1]  

示例

|示例|解释|
|:--|:--|
|<code>button[@text~’sample[0-9]’]</code>|匹配以下按钮元素：`'sample0'，'sample1'，...'sample9'，'Mysample26'`|
|<code>listitem[@text~’^sample’]</code>|匹配以文本值为`sample`开头的所有元素|
|<code>listitem[@text~’sample$’]</code>|匹配以文本值为`sample`结尾的所有元素|
|<code>listitem[@text~’gr(a&#124;e)y’]</code>|匹配文本值`gray`或`grey`|
|<code>listitem[@text~’^sample 123$’]</code>|匹配`'样本123'`（使用反斜杠来规避特殊字符，例如空格）|
|<code>listitem[@text~’^(?i:MyTeXt)$’]</code>|外部匹配正则表达式不区分大小写，例如 'mytext'，'MYTEXT'，'mYTeXT'，...或包含用户名和密码组合的数据库进行测试|

## 需要转义的字符

以下是在正则表达式中使用前缀为反斜杠时需要转义的特殊字符。例如。当你想匹配文本'Sample。'（末尾有一个点）时，需要对点进行转义：'Sample.'。  

|字符|说明|
|--|--|
|`·`|点将匹配任何单个字符。例如`'Sample.'`匹配：`Sample1`、`Samplex`等|
|`$`|美元符号将匹配字符串的结尾。表达式`'abc $'`只有`abc`在字符串末尾时才匹配|
|`\`|修改字符允许其一侧的任何表达式匹配目标字符串。<code>'gr(a&#124;e)y'</code>的表达式可以与`gray`或`grey`匹配|
|`*`|星号表示表达式中星号左边的字符应该匹配零次或多次。例如`'go*gle'` 匹配：`ggle`、` gogle`、`google`、`gooogle`等|
|`+`|加号类似于星号，但表达式中+号左边必须至少有一个字符匹配。例如`'go+gle'`匹配：`gogle`、`google`、`gooogle`等|
|`?`|问号(`?`)匹配左边的字符0或1次。例如`'colo?r'`匹配：`color`和`colour`|
|`^`|匹配字符串的开头。表达式`'^A'`仅匹配在字符串开头的`A`|
|`()`|括号影响正则表达式匹配的顺序|
|`[]`|包含一组字符的括号表明所包含的任何字符都可能与目标字符匹配|
|`[^0-9]`|左括号后面的插入符号有不同的含义。它用于排除括号内的其余字符以匹配目标字符串。`[^0-9]`的表达表明目标字符必须不是一个数字。|



[0]: https://www.ranorex.com/help/latest/ranorex-studio-expert/regular-expressions-ranorexpath/  
[1]: https://docs.microsoft.com/zh-cn/dotnet/standard/base-types/regular-expression-language-quick-reference

