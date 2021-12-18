# 秘银介绍和环境设置

> 原文:[https://www . geesforgeks . org/mithril-js-introduction-and-environment-setup/](https://www.geeksforgeeks.org/mithril-js-introduction-and-environment-setup/)

**Mithril** 是一个客户端 JavaScript 框架，用于创建单页应用程序。还有很多其他流行的框架，那些已经足够流行并且有巨大的社区支持的，比如 [React、](https://www.geeksforgeeks.org/react-js-introduction-working/) [Vue](https://www.geeksforgeeks.org/vue-js-introduction-installation/) 、 [](https://www.geeksforgeeks.org/vue-js-introduction-installation/) 和 [Angular](https://www.geeksforgeeks.org/introduction-to-angularjs/) 。那你为什么要选择 Mithril 而不是那些神奇的表演者框架呢？Mithril 涵盖了其他框架提供的所有特性，如 DOM 元素、组件、路由和 XHR。XHR 只是和服务器沟通的一种方式，沟通才是进步最重要的。

**选择 Mithril 而非领先框架的理由:**

*   **尺寸:**与那些框架相比，秘银的尺寸非常小，秘银的总尺寸为 9.5Kb，它涵盖了所有的功能。其中其他框架的大小为(React+React Router+Redux+fetch)→64Kb，(Vue+Vue-Router+Vuex+fetch)→40kb，Angular→135kb。
*   **性能:**Mithril 的性能最好，因为它只需要 6.4 毫秒，其他框架在 React 中需要 12.1 毫秒左右，在 Vue 中需要 9.8 毫秒，在 Angular 中需要 11.5 毫秒。

**注意:**如果你的团队已经在其他框架中，并且你的客户的产品完全基于另一个框架，那么继续你所拥有的，但是你正在学习一个新的框架或者想要创建一个紧凑和快速的世界，那么 Mithril 是正确的选择。

**要求/安装模块:**要开始使用 Mithril，我们可以使用 CDN 链接或使用 npm 命令进行安装，这两种方式解释如下:

**CDN 链接:**可以在 HTML 文件中使用一个 CDN 链接，然后继续。在脚本标签中复制下面的链接。

```
https://unpkg.com/mithril/mithril.js
```

**NPM 模块:**使用以下命令安装秘银模块:

```
npm install mithril --save
```

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src="https://unpkg.com/mithril/mithril.js">
    </script>
</head>

<body>
    <script>
        var root = document.body

        // Rendering a String as an Output
        m.render(root, 
"GeeksforGeeks A Computer Science portal for Geeks")
    </script>
</body>

</html>
```

**输出:**

![](img/93321925a8fbd2ac3f3cc62b9c0e57c4.png)

**参考:**T2】https://mithril.js.org/