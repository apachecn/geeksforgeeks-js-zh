# 如何更新 package.json 文件中的依赖关系？

> 原文:[https://www . geesforgeks . org/如何更新包中依赖项-json-file/](https://www.geeksforgeeks.org/how-to-update-dependency-in-package-json-file/)

在本文中，我们将讨论如何用 npm 更新项目的依赖关系。您一定听说过 [npm](https://www.geeksforgeeks.org/node-js-npm-node-package-manager/) ，它被称为节点包管理器。因此，我们可以运行这个命令来安装一个 npm 包。

```
npm install
```

**注意:**节点 5.0.0 版本后不再需要–save 标志。

该包已安装，应在`package.json`文件所在的同一目录下的 node_modules 文件夹中找到。带版本的包名条目应在`package.json`和`package-lock.json`中找到。您可以在`package.json`文件中看到包的当前版本。您可以在`package.json`文件中找到最新版本的 npm。

如果你想添加一个特定的版本，你可以运行 npm install @ version _ 在这里像`npm install react@^1.8.5`

```
{
    "dependencies": {
        "react": "^1.8.5"
    }
}
```

如果您想添加最新版本，您可以运行`npm install`或`npm install @latest`。

```
{
    "dependencies": {
        "react": "^16.12.0"
    }
}
```

通过查看这两个文件，我们清楚地知道我们有 16.12.0 版本的 react，未来更新的规则是^.这个规则意味着在未来 npm 只能更新到补丁和小版本。

将来，如果有新的补丁或小版本，当我们键入 npm update 命令时，已经安装的版本将得到更新，`package-lock.json`也将通过填充新版本同时得到更新。很明显，只有`package-lock.json`文件会被更新，而`package.json`不会。

要获得到目前为止新版本或过时包的完整列表，我们必须运行这个命令

```
npm outdated
```

通过运行 npm update，它将不会更新主要版本的版本，因为主要版本从未以这种方式更新，因为其中一些版本可能会在您的实时 web 应用程序中引入重大更改，因此 npm 不想惹麻烦。

要更新软件包的新版本和主要版本，您必须全局安装 npm-check-updates 软件包。

```
npm install -g npm-check-updates
```

安装软件包后，运行以下命令:

```
ncu
```

它将显示当前目录中的新依赖项，而运行此命令将列出所有具有新版本的全局包。

```
ncu -g
```

现在运行这个命令:

```
ncu -u
```

运行此命令后，将导致升级`package.json`文件中的所有版本提示，因此 npm 将使用此方法安装主要版本。

现在一切都结束了。只需运行更新命令:

```
npm update
```

如果您有一个没有任何 node_modules 依赖项的新项目，并且您想要安装新版本，那么运行以下命令:

```
npm install
```