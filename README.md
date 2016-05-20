# DocumentingSwift
在Xcode中使用MarkDown给Swift代码写注释
[原文地址](http://www.appcoda.com/swift-markdown/)

####一个好的文档有如下几个作用：

* 在细节层次上描述相应属性、函数、类所实现的功能，或者所达到的目的。此外，文档是突出显示特定条件最佳的地方，你所写的函数的例子或需求。
* 突出你函数的输入和输出（参数、返回值）。
* 当你数月后重新再看项目最初的实现时，可以记住每个函数的功能，以及每个属性的意义。
* 当你分享你的Libraries的时候，让其它开发者很容易的理解如何使用你的代码。
* 生产出专业的指南使用工具

####在Xcode中写的文档一般可以有三种方法预览或进入

* 按住Option键，单击属性、函数、Class的名字等等。快速预览弹窗会在名字的周边弹出来。
* 将光标放在函数、属性、Class名字上，打开快速帮助查阅
* 使用第三方工具将为你产生一个指南。

####MarkDown语法
* ``` ##text## ``` --> 标题（#与H1对应，## 与H2对应，以此类推）
* ``` ** text ** ``` --> **加粗，text与“ * ”之间无空格**
* ``` * text * ``` --> *斜体，text与“ * ”之间无空格*
* ``` * text ``` --> 每行字前面加黑点
* ```4个空格``` --> 代码块
* ``` [linked text] (http://some-url.com)``` --> 网址链接
* ``` (三个`)text(三个`) ``` --> 代码块

####MarkDown编辑器
[StackEdit (Online)](https://stackedit.io)

[Typora](https://www.typora.io)

[Macdown](http://macdown.uranusjr.com)

[Focused](https://71squared.com/focused)

[Ulysses](http://www.ulyssesapp.com)

####使用MarkDown编写注释

**注释单行**

```
/// Your Code Document
```
**注释多行（函数、结构体等）**

```
/**

 */
```
####代码注释见Playground
查看代码注释效果方法：

按住 Option 键，光标放在加了注释的property、Method、Class上，当光标变为“?”样式时，左键单击即可弹出注释。

###第三方工具[Jazzy](https://github.com/realm/jazzy)
Jazzy是一款将你的OC、Swift代码，生成Apple-style文档的工具。(把代码及注释生成Html文档查看)

安装：
	
```
[sudo] gem install jazzy
```
使用Jazzy根据代码以及注释生成文档：
[示例Demo](https://github.com/appcoda/SwiftDocSample.git)

```
// 进入项目根目录
cd path_to_project_folder

// 生成文档
jazzy --min-acl internal

// 双击打开
```

指定另外一个版本(旧版本)的swift

```
jazzy --swift-version 2.1.1 --min-acl internal
```

结果如下图所示:
![result]()