# Ember.js 简介

> 原文:[https://www.geeksforgeeks.org/ember-js-introduction/](https://www.geeksforgeeks.org/ember-js-introduction/)

Ember.js 是一个**开源 JavaScript** 框架，用于开发大型**客户端 web 应用**，基于**模型-视图-控制器** ( **MVC)** 架构。Ember 旨在减少开发时间并提高生产率，它是全球范围内采用的发展最快的前端应用程序框架之一。它目前在许多网站上使用，如 Square、话语、Groupon、Linked In、Live Nation、Twitch 和 Chipotle。

虽然被认为是网站的框架，但 Ember 也可以用来开发桌面和移动应用程序。如果您想构建一个单页 web 应用程序，Ember.js 是您的正确选择。最著名的烬桌面应用程序的例子是苹果音乐。

**什么是客户端框架？**

客户端框架通常是一个 JavaScript 库，支持网页和客户端浏览器的增强和操作，例如 **React** 、 **Angular** 、 **Vue** 、 **Ember** 、**T9】和**主干**。**

**什么是 MVC？**

MVC 是由三个相互关联的部分组成的软件设计模式。它们包括用于开发用户界面的**模型**(数据)**视图**(用户界面)和**控制器**(处理输入的进程)。

**为什么是 Ember.js？**

*   它允许通过提供包含数据管理和应用程序流的完整解决方案来构建客户端 JavaScript 应用程序。
*   约定胜于配置。
*   一个灵活的框架，允许您加快应用程序的性能，而不必不断地重新加载整个页面。
*   完全支持数据绑定，这意味着如果一个值被更改，另一个值会自动更新。
*   自动确定路线和控制，以及允许共享的网址。

**如何安装 Ember.js？**

Ember CLI(命令行界面)是用 JavaScript 构建的，需要 Node.js 运行时。因此，如果您的计算机安装了 Node.js，您就可以开始了。如需安装[点击此处](https://nodejs.org/en/download/)查看版本确认:

```
node -v
npm -v
```

您可以使用 npm，即 Node.js 包管理器，用一个命令安装 Ember。将此输入您的终端:

```
npm install -g ember-cli
```

**如何创建项目？**

**步骤 1:** 要使用 Ember CLI 创建新项目，请在命令提示符下使用**“新建”**命令。让我们考虑一下我们项目的名称**“烬 _ 项目”**。创建新项目后，更改您的目录。

```
ember new ember_project
cd ember_project
```

**步骤 2:** 现在我们需要使用任何代码编辑器在**app/templates/application . HBS**文件中进行更改(删除{{welcome-page}}组件):

## 超文本标记语言

```
<div class="intro">
      <h1>Welcome to GeekforGeeks!</h1>

<p>Ember.js is fun!</p>

</div>
```

**第三步:**然后我们可以通过在命令提示符下输入以下代码来启动烬**开发服务器**:

```
ember serve
```

**第四步:**上述查询执行成功后，您可以在 [http://localhost:4200/](http://localhost:4200/) 上查看自己的进度。

**输出:**

![](img/8254f68a83912f89e95d73dcd1a0aa99.png)

参考:guides.emberjs.com

**优势:**

*   极高的一致性和简单的配置
*   内置路由器
*   自己的调试工具(烬检查器)
*   全栈开发选项
*   双向数据绑定

**缺点:**

*   学习曲线陡峭。烬对初学者来说并不容易。
*   在处理 Ember Js 框架时不能重用组件
*   最硬最重的框架之一。
*   不适合小项目。
*   有大量与烬相关的内容和例子已经过时。