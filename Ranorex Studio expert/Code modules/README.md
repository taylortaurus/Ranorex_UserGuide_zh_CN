# [译] 代码模块

*原文地址 👉 [Code modules][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-7-10*    
*♋ update time : 2018-7-10*  

---  

虽然只有智能操作、变量和用户代码功能的Ranorex录制足以创建健壮的测试自动化模块，但是编写纯粹的Ranorex自动化代码可能是有用的或更可取的。
在下一节中，您将了解如何创建一个新的代码模块，该模块将向KeePass应用程序添加新的凭据数据集的过程自动化测试。


## 创建代码模块  

单击工具栏上的“添加代码模块”按钮创建一个新的代码模块。  

![C4000-0000010](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudioExpert/C4000-0000010.png)  

或者，您可以使用Test Suite中的上下文菜单添加新的代码模块。  

![C4000-0000020](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudioExpert/C4000-0000020.png)  

![C4000-0000030](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudioExpert/C4000-0000030.png)  
*指定用于代码模块的名称*  

单击“创建”按钮后，新文件将添加到项目中，并在文件视图中自动打开。Ranorex Studio创建了一个新的测试模块类，其中包含一个“Run”方法，可以使用测试自动化代码进行扩展。  
  
*C#*  
```clike
namespace KeePass
{
    /// <summary>
    /// Description of AddCredentialEntry.
    /// </summary>
    [TestModule("03F5603B-0DDC-49AA-8C26-4D8088260C66", ModuleType.UserCode, 1)]
    public class AddCredentialEntry : ITestModule
    {
    /// <summary>
    /// Constructs a new instance.
    /// </summary>
        public AddCredentialEntry()
        {
        // Do not delete - a parameterless constructor is required!
        }
        /// <summary>
        /// Performs the playback of actions in this module.
        /// </summary>
        /// <remarks>You should not call this method directly, instead pass the module
        /// instance to the <see cref="TestModuleRunner.Run(ITestModule)"> method
        /// that will in turn invoke this method.</see></remarks>
        void ITestModule.Run()
        {
            Mouse.DefaultMoveTime = 300;
            Keyboard.DefaultKeyPressTime = 100;
            Delay.SpeedFactor = 1.0;
        }
    }
}

```  
  
*VB.NET*  
```clike
Namespace KeePass
''' <summary>
''' Description of AddCredentialEntry.
''' </summary>
<testmodule("03f5603b-0ddc-49aa-8c26-4d8088260c66", moduletype.usercode,="" 1)=""> _
Public Class AddCredentialEntry
Implements ITestModule
''' <summary>
''' Constructs a new instance.
''' </summary>
' Do not delete - a parameterless constructor is required!
Public Sub New()
End Sub
''' <summary>
''' Performs the playback of actions in this module.
''' </summary>
''' <remarks>You should not call this method directly, instead pass the module
''' instance to the <see cref="TestModuleRunner.Run(ITestModule)"> method
''' that will in turn invoke this method.</see></remarks>
Private Sub ITestModule_Run() Implements ITestModule.Run
Mouse.DefaultMoveTime = 300
Keyboard.DefaultKeyPressTime = 100
Delay.SpeedFactor = 1.0
End Sub
End Class
End Namespace
</testmodule("03f5603b-0ddc-49aa-8c26-4d8088260c66",>
```

## 在代码模块中使用控件库  

以同样的方式在录制模块中使用控件库来识别用于自动化的UI元素，您也可以在代码中使用它。只需将代表控件库的新私有成员添加到您的代码模块类，如下所示：
  
*C#*
```clike
public class AddCredentialEntry : ITestModule
{
    // Repository object to access UI Elements
    MyFirstTestProjectRepository MyRepo = MyFirstTestProjectRepository.Instance;
    /// Constructs a new instance.
    public AddCredentialEntry()
    {
        // Do not delete - a parameterless constructor is required!
    }
    void ITestModule.Run()
    {
        Mouse.DefaultMoveTime = 300;
        Keyboard.DefaultKeyPressTime = 100;
        Delay.SpeedFactor = 1.0;
        // Click 'Add Entry' Button MainMenu
        MyRepo.MainForm.Edit.Click();
        MyRepo.KeePass.AddEntry.Click();
        // Set text fields
        MyRepo.AddEntry.TabSheetAddEntry.Title.TextValue = "WordPressDemo";
        MyRepo.AddEntry.TabSheetAddEntry.UserName.TextValue = "admin";
        MyRepo.AddEntry.TabSheetAddEntry.Password.TextValue = "demo123";
        MyRepo.AddEntry.TabSheetAddEntry.Repeat.TextValue = "demo123";
        MyRepo.AddEntry.TabSheetAddEntry.URL.TextValue = "bitly.com/wp_demo";
        // Choose an icon
        MyRepo.AddEntry.TabSheetAddEntry.MBtnIcon.Click();
        MyRepo.IconPicker.LI_Icon.Click(Location.CenterLeft);
        MyRepo.IconPicker.ButtonClose.Click();
        // Set Expires
        MyRepo.AddEntry.TabSheetAddEntry.MBtnStandardExpires.Click();
        MyRepo.KeePass.MI_Expires.Click();
        // Save Credential Entry
        MyRepo.AddEntry.ButtonOK.Click();
    }
}
```
  
*VB.NET*
```clike
Public Class AddCredentialEntry
Implements ITestModule
' Repository object to access UI Elements
Private MyRepo As MyFirstTestProjectRepository = MyFirstTestProjectRepository.Instance
''' Constructs a new instance.
' Do not delete - a parameterless constructor is required!
Public Sub New()
End Sub
Private Sub ITestModule_Run() Implements ITestModule.Run
Mouse.DefaultMoveTime = 300
Keyboard.DefaultKeyPressTime = 100
Delay.SpeedFactor = 1.0
' Click 'Add Entry' Button MainMenu
MyRepo.MainForm.Edit.Click()
MyRepo.KeePass.AddEntry.Click()
' Set text fields
MyRepo.AddEntry.TabSheetAddEntry.Title.TextValue = "WordPressDemo"
MyRepo.AddEntry.TabSheetAddEntry.UserName.TextValue = "admin"
MyRepo.AddEntry.TabSheetAddEntry.Password.TextValue = "demo123"
MyRepo.AddEntry.TabSheetAddEntry.Repeat.TextValue = "demo123"
MyRepo.AddEntry.TabSheetAddEntry.URL.TextValue = "bitly.com/wp_demo"
' Choose an icon
MyRepo.AddEntry.TabSheetAddEntry.MBtnIcon.Click()
MyRepo.IconPicker.LI_Icon.Click(Location.CenterLeft)
MyRepo.IconPicker.ButtonClose.Click()
' Set Expires
MyRepo.AddEntry.TabSheetAddEntry.MBtnStandardExpires.Click()
MyRepo.KeePass.MI_Expires.Click()
' Save Credential Entry
MyRepo.AddEntry.ButtonOK.Click()
End Sub
End Class
```  

> **注意：**  
> 默认情况下，存储库的类名与项目视图中显示的存储库文件名（* .rxrep）相同。
  
现在，该类使用私有成员来引用存储库，以便在“Run”方法中重用一些对象（“Title”，“Username”，“Password”，“PasswordRepeat”和“URL”）。  

![C4000-0000040](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudioExpert/C4000-0000040.png)  

根据存储库的结构，访问代码中的项可能会变得越来越复杂。为了降低复杂性-尤其是在多次使用UI元素时-您应该使用局部变量，而不是每次需要自动化UI元素时编码存储库的整个结构。  

*C#*
```clike
var ButtonOK = MyRepo.FormAdd_Entry.ButtonOK;
ButtonOK.Click();
```  
  
*VB.NET*
```clike  
Dim ButtonOK = MyRepo.FormAdd_Entry.ButtonOK
ButtonOK.Click()
```  

要创建如上面代码中所示的局部变量，只需将存储库浏览器中的元素直接拖放到代码中即可。  

> **注意：**  
> 如果存储库本身不是该类的一部分（例如，新创建的代码模块），则也会生成存储库的本地变量。  

## 访问代码模块中的屏幕截图  

从Ranorex 3.3开始，可以使用存储库项目的Info对象直接在代码中访问屏幕截图。 例如，如果您要将捕获的屏幕截图与测试中的应用程序的实际外观进行比较，这将非常有用。  

> **注意**  
> 如果您选择基于图像记录，将自动捕获屏幕截图。在此处获取更多信息：⇢[基于图像的自动化][1]。  

![C4000-0000050](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudioExpert/C4000-0000050.png)  
*控件库中捕获的截图*  

*C#*
```clike
// get the screenshot from the repository
Bitmap MyScreenshot = MyRepo.IconPicker.LI_IconInfo.GetScreenshot_Icon();
// create FindOptions with similarity set to 95%
Imaging.FindOptions MyFindOptions = new Imaging.FindOptions(0.95);
// compare the captured screenshot with the actual list item
Validate.CompareImage(MyRepo.IconPicker.LI_Icon, MyScreenshot, MyFindOptions);
```  
  
*VB.NET*
```clike  
' get the screenshot from the repository
Dim MyScreenshot As Bitmap = MyRepo.IconPicker.LI_IconInfo.GetScreenshot_Icon()
' create FindOptions with similarity set to 95%
Dim MyFindOptions As New Imaging.FindOptions(0.95)
' compare the captured screenshot with the actual list item
Validate.CompareImage(MyRepo.IconPicker.LI_Icon, MyScreenshot, MyFindOptions)
```  
  
> **注意：**  
> 使用FindOptions，您可以设置“相似性”等自定义值。 此选项允许您定义要搜索的图像区域与屏幕截图相同的最小相似度，以便被视为匹配。 有关详细信息，请查看
> ⇢[基于图像的自动化][1]。  


## 在代码模块中使用变量  

要使用代码模块中数据连接器提供的值，需要在代码中添加变量。使用上下文菜单项“插入模块变量”。

![C4000-0000060](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudioExpert/C4000-0000060.png)  
*在代码模块中添加一个新变量*  

![C4000-0000070](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudioExpert/C4000-0000070.png)  
*指定变量名称和默认值*  

通过添加新变量Ranorex Studio在当前光标位置插入新的代码片段。变量实现由公共属性和私有成员”组成。  

*C#*  
```clike
string _varTitle = "Wordpress Credentials";
[TestVariable("9348A7E6-80B6-4A2B-9CBF-0276A236AA3E")]
public string varTitle
{
    get { return _varTitle; }
    set { _varTitle = value; }
}
```  
  
*VB.NET*  
```clike  
Private _varTitle As String = "Wordpress Credentials"
<testvariable("9348a7e6-80b6-4a2b-9cbf-0276a236aa3e")> _
Public Property varTitle() As String
Get
Return _varTitle
End Get
Set
_varTitle = value
End Set
End Property
</testvariable("9348a7e6-80b6-4a2b-9cbf-0276a236aa3e")>
```  

现在为“用户名”，“密码”和“URL”创建其他变量。 所有模块变量将立即出现在模块浏览器中。  

![C4000-0000080](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudioExpert/C4000-0000080.png)  

### 使用Setter方法访问存储库变量  

要在通过代码模块访问控件库元素时将控件库变量绑定到外部数据，您必须创建一个新的模块变量来充当桥接器。您可以使用公共变量的setter方法来设置控件库变量。  

存储库使用的变量(例如，KeePass的“添加条目对话框”上下文菜单中的菜单项的“varExpires”)可以通过存储库轻松访问，甚至可以通过代码访问。为了将这些变量绑定到外部数据(例如Excel文件中的一行)，您必须创建一个新的模块变量来充当外部数据和存储库变量之间的桥梁。遵循这种方法，显然最好将setter方法用于公共变量。每当设置该变量的值时，都会调用一个公共变量的setter方法。即为私有变量赋值，为公共属性保存信息。为了设置存储库变量，可以很容易地扩展这个方法。  

前两个新模块变量“varExpires”和“varIconIndex”必须以与“varTitle”、“varPassword”相同的方式创建。之后，必须将一个简单的代码行插入到每个变量的setter方法中。此代码行用于将传递的值分配给存储库变量，并便于绑定到外部数据。 \
  
*C#*
```clike
string _varRepoIconIndex = "1";
[TestVariable("EF09BC93-3447-4AC2-9DEB-FE3D78ED5538")]
public string varRepoIconIndex
{
    get { return _varRepoIconIndex; }
    set {
        _varRepoIconIndex = value;
        // Additionally set the Repository Variable in Setter-Method
        MyRepo.varIconIndex = _varRepoIconIndex;
    }
}
    string _varRepoExpires = "1 Year";
    [TestVariable("D0A54427-68FF-4B9D-B861-4882BCEC846B")]
    public string varRepoExpires
    {
    get { return _varRepoExpires; }
    set {
    _varRepoExpires = value;
    // Additionally set the Repository Variable in Setter-Method
    MyRepo.varExpires = _varRepoExpires;
    }
}
```  

*VB.NET*
```clike
Private _varRepoIconIndex As String = "1"
<testvariable("ef09bc93-3447-4ac2-9deb-fe3d78ed5538")> _
Public Property varRepoIconIndex() As String
Get
Return _varRepoIconIndex
End Get
Set
_varRepoIconIndex = value
' Additionally set the Repository Variable in Setter-Method
MyRepo.varIconIndex = _varRepoIconIndex
End Set
End Property
Private _varRepoExpires As String = "1 Year"
<testvariable("d0a54427-68ff-4b9d-b861-4882bcec846b")> _
Public Property varRepoExpires() As String
Get
Return _varRepoExpires
End Get
Set
_varRepoExpires = value
' Additionally set the Repository Variable in Setter-Method
MyRepo.varExpires = _varRepoExpires
End Set
End Property
</testvariable("d0a54427-68ff-4b9d-b861-4882bcec846b")></testvariable("ef09bc93-3447-4ac2-9deb-fe3d78ed5538")>
```  

因此，Excel文件中的两列可以绑定到这些模块变量。 此绑定会导致在测试用例中为每次迭代设置变量。 设置这些变量时，扩展功能还会设置存储库变量，以确保在我们的示例中使用和单击正确的图标。  

### 在测试用例中使用代码模块

上面实现的代码模块现在可以由测试用例运行。 添加一个新的测试用例（'TC_AddEntryFromCode'）到您的测试套件并重用已有的模块来启动KeePass，在开始时登录并在测试用例结束时验证，删除，保存和关闭它。 您可以使用拖放操作将新创建的代码模块快速插入测试用例。  

![C4000-0000090](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudioExpert/C4000-0000090.png)  
*将代码模块拖放到测试用例中并将其与录制模块组合*

现在，您可以使用新的测试用例重用在数据驱动测试期间创建的现有数据连接器。
![C4000-0000100](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudioExpert/C4000-0000100.png)  
*通过从下拉列表中选择项目来重用现有数据连接器*  

![C4000-0000110](https://gitee.com/taylortaurus/RX_UserGuide_GitBook_Picbed/raw/master/RanorexStudioExpert/C4000-0000110.png)  
*将新创建的变量绑定到数据连接器的列，即Excel文件中的列*



[0]: https://www.ranorex.com/help/latest/ranorex-studio-expert/code-modules/
[1]: ..\\..\\..\\Ranorex%20Studio%20advanced/Image-based%20automation/index.html

