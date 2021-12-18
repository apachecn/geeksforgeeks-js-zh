# 烬 js 安装

> 原文:[https://www.geeksforgeeks.org/ember-js-installation/](https://www.geeksforgeeks.org/ember-js-installation/)

基本上，Ember.js 是一个开源的 JavaScript 框架，由 Yehuda Katz 为富有创造力和雄心的网络开发人员开发。这是一个开发现代网络应用程序的 Java-Script 框架，它结合了您需要的一切来构建在任何设备上工作的高级用户界面。Ember.js 有一个非常有用的数据管理系统，可以帮助您在客户端组织数据并与服务器通信。

在开始使用 Ember.js 之前，我们需要将其安装在您的本地系统上。Ember.js 使用命令行界面(CLI)工具，通过使用 CLI 可以创建和构建您的 Ember 项目。Ember CLI 处理现代应用程序资产管理，如连接、缩小和版本控制，它还提供生成器来生成组件、路由等。

**附加条件:**安装 Ember CLI 需要有以下依赖项:

*   [去](https://www.geeksforgeeks.org/introduction-and-installation-of-git/)
*   t8〔节点〕。联署材料你好 NPM 的。

**烬 JS 的安装:**

**步骤 1:** 在安装 Ember CLI 工具之前，您需要在本地计算机上安装节点和 [npm](https://www.geeksforgeeks.org/node-js-npm-node-package-manager/) 。你可以从它的[官方](https://nodejs.org/en/download/)网站安装 NodeJS。

之后，您可以键入以下命令来检查节点和 npm 的版本。

```
node -v
npm -v
```

**步骤 2:** 安装完节点和 npm 后，可以在本地计算机上运行以下命令来安装 Ember CLI。

```
npm install -g ember-cli
```

**注:** *-g* 表示我们可以全球安装。

要安装所需版本，请使用以下命令:

```
npm install -g ember-cli@3.20.0
```

**步骤 3:** 成功安装烬 CLI 工具后，需要检查烬的版本，使用以下命令:

```
ember -v
```

执行上述命令后，它将显示如下所示的烬版本。

```
ember-cli: 3.20.0
node: 14.17.1
```

获得这个输出后，我们知道 Ember CLI 已经成功安装在我们的系统中。现在我们可以到处使用它。