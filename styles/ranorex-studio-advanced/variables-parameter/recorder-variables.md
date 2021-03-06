# [译] 录制器变量

*原文地址 👉 [Recorder variables][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-9-17*    

---

**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [变量标识](#变量标识)
- [定义录制器变量](#定义录制器变量)
- [默认变量值](#默认变量值)
- [录制器变量管理](#录制器变量管理)

## 变量标识

在用变量替换常数值之前，有必要确定可能的和有用的变量候选。下图是假设要插入人员数据的数据库表单。

![B1020-0000042](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/B1020-0000042.png)  
*录制器变量示例*  

**要点须知** 
1. 在本例中，第一个名称、最后一个名称和年龄的文本常量值可以用录制器变量替换
2. Ranorex中的变量由变量名前面的$来标识
3. 命名约定和变量管理由你的测试团队控制

## 定义录制器变量

![B1020-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/B1020-0000050.png)  
*定义录制器变量*  

1. 选择要定义变量的录制器动作，并从常量值右打开下拉列表。单击`As new variable`以启动变量定义
2. 为变量指定一个有意义的名称并使用`OK`进行确认
3. 看到绿色显示变量名替换原来的常量值

## 默认变量值

最初设置的值(即已记录的)将自动预先设置为默认变量值。在我们的示例中，最初记录的文本值`John`因此被设置为默认值。默认值可以随意更改。

![B2020-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/B2020-0000010.png)  
*录制器变量默认值*  

**提示**  
> 如果变量没有绑定到任何数据，则应用默认值。因此，请谨慎地选择默认值。

## 录制器变量管理  

录制器变量可以通过在录制器视图中，单击打开变量编辑器来管理。

![B2020-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/B2020-0000020.png)  
*打开录制器变量管理器*  

1. 选择并打开一个包含变量的录制模块
2. 单击录制器工具栏中的`Variables`按钮来打开变量编辑器

**提示**  
> 只有当前录制模块的变量才显示在变量编辑器里

![B2020-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/InterfacesAndConnectivity/B2020-0000030.png)  
*录制器变量编辑器*  

1. 变量名绑定默认变量
2. 变量编辑器工具栏 
    - 用来复制和粘贴的菜单
    - 直接新增变量按钮
    - 移除不在使用的变量（变量清理） 
    - 从当前录制模块中的控件库里拷贝一个变量（如果变量存在的话）
3. 变量提示
    -  `Variable in use`: 分配到动作中正在使用的变量
    -  `Variable in use from repository`: 显示录制模块里控件库中正在使用变量
    -  `Variable not in use`: 变量已被定义，但是没有分配到动作项中 







[0]: https://www.ranorex.com/help/latest/ranorex-studio-advanced/variables-parameter/recorder-variables/
