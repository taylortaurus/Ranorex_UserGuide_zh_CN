# [译] Selenium Webdriver 集成

*原文地址 👉 [Selenium Webdriver integration][0]*

*@ translator : [TaylorTaurus](https://github.com/taylortaurus)*    
*♋ translate time : 2018-7-8*    
*♋ update time : 2018-9-18*  

---

使用Selenium WebDriver集成，您可以在不同的浏览器、操作系统和机器上运行Ranorex创建的web测试，而无需任何插件或附加组件。

Ranorex使用现有的Selenium WebDriver基础架构运行web测试，可以运行在如下平台:

- 微软的Internet Explorer，微软Edge，谷歌Chrome, Mozilla Firefox，以及微软Windows上的Chromium
- 苹果Safari，谷歌Chrome和Mozilla Firefox在苹果macOS上
- Linux上的谷歌Chrome和Mozilla Firefox

**提示** 
> Web测试仍然必须在本地记录。你需要RanorexStudio,本地安装的web浏览器与激活Ranorex自动化插件,和您的本地计算机必须设置为自动化根⇢端点列表。Ranorex Studio支持以下操作系统+浏览器组合来进行web测试记录:Microsoft Windows + Microsoft Internet Explorer、谷歌Chrome、Mozilla Firefox和Chromium。


**本章导视，章节内段落跳转推荐使用右上角的锚点！**

- [Ranorex中Selenium WebDriver集成的快速指南](#Ranorex中SeleniumWebDriver集成的快速指南)
- [建立Selenium WebDriver基础架构](#建立SeleniumWebDriver基础架构)
- [运行Selenium服务](#运行Selenium服务)
- [网络测试指南](#网络测试指南)


## Ranorex中SeleniumWebDriver集成的快速指南

1. 👉 [安装](#建立SeleniumWebDriver基础架构)Selenium WebDriver基础架构
2. 👉 [启动](#运行Selenium服务)Selenium 独立服务器
3. 👉 [添加网页驱动端点][5]到Ranroex Stduio
4. 在你本地的机器上录制你的网页测试或是直接使用现有的
5. 回顾网页测试 👉 指南
6. 设定网页驱动端点作为 👉 自动化根节点
7. 运行测试套件

## 建立SeleniumWebDriver基础架构

这一章只提供了一个基本的介绍。有关Selenium WebDriver基础架构的完整文档请访问官网 👉 [Selenium官网][1]

对于基本的安装，你需要：

- Java运行时环境
- 一个Selenium服务器  
    - [下载][3]最新版本的Selenium Standalone Server并放入文件夹中
- 你想要进行Selenium Server自动化的网页浏览器的驱动程序
    - 所有相关的链接和安装步骤可以在[这里][2]获取 
    - 下载适用于您平台的正确驱动程序，根据需要解压缩，并放入与Selenium Standalone Server相同的文件夹中

**提示**  
> Internet Explorer Driver需要进行多项[设置][3]才能正常工作

## 运行Selenium服务

在添加端点或运行测试之前，您需要启动服务器。

打开命令行控制台并切换到包含Selenium Standalone Server的文件夹。执行以下命令：

```java
java -jar selenium-server-standalone-.jar
```

将“”替换为下载的Selenium Standalone Server文件的版本号。 窗户必须保持打开状态。

## 网络测试指南

Selenium WebDriver与Ranorex为基于桌面的Web测试提供的Web测试功能不同。在本地Web浏览器上录制Web测试后，请按照以下步骤使其与Selenium WebDriver兼容执行：

- 删除与Web浏览器应用程序本身交互的所有操作和存储库项
- 使用“关闭应用程序”操作关闭Web浏览器
- 另请参阅Ranorex 7.0[发行说明][4]。 它们包含有关Selenium WebDriver集成的重要信息




[0]: https://www.ranorex.com/help/latest/interfaces-connectivity/selenium-webdriver-integration/
[1]: http://www.seleniumhq.org/
[2]: http://www.seleniumhq.org/download/
[3]: https://github.com/SeleniumHQ/selenium/wiki/InternetExplorerDriver#required-configuration
[4]: http://release-notes.html/#c16310
[5]: ..\\..\\..\\Web_and_mobile_testing/Endpoints/[译]添加一个WebDriver端点.html

