# 三合一入门

> 原文:[https://www.geeksforgeeks.org/introduction-to-three-js/](https://www.geeksforgeeks.org/introduction-to-three-js/)

你有没有想过这些图形和游戏是如何在网络浏览器上运行的？它背后的主要技术是什么？当然，仅仅使用 HTML 和 CSS 是不可能的。前几天我们用 [WebGL](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API) 做这个任务。网络图形库是一个 JavaScript 应用编程接口，用于在网络浏览器上渲染三维对象、二维对象和图形。WebGL 应用编程接口允许用户在网页上体验交互式内容，具有图形处理器加速，而不必首先下载或安装任何插件。对于开发人员来说，WebGL 提供了对硬件的低级访问，具有熟悉的 OpenGL ES 的代码结构。

WebGL 是由 Mozilla 组织创建的。有了 WebGL 的所有这些好处，WebGL 也有一些缺点，其中[](https://threejs.org/)**起了作用。WebGL 是一个非常低级的系统，它只绘制像点、正方形和线这样的基本对象。用 WebGL 做任何有意义的事情通常需要相当多的代码，这就是**三个 js** 的用武之地。**

****什么是三个 j？****

**[Three.js](https://threejs.org/) 是一个开源的 JavaScript 库，用于在网络浏览器上显示图形、3D 和 2D 对象。它使用场景背后的 WebGL API。三个 js 允许你使用你的 GPU(图形处理单元)在网络浏览器的画布上渲染图形和三维对象。因为我们正在使用 JavaScript，所以我们也可以与其他 HTML 元素进行交互。里卡多·卡韦略于 2010 年 4 月发布了《Three.js》。**

****为什么要用三个 js？****

***   Because Three.js is open source, we can easily view the source code and understand the function of the code (function).*   When we use WebGL for graphics, it doesn't support most browsers, but Three.js supports most browsers.*   It doesn't need any third-party plug-ins to run the code.*   You only need to work in a programming language JavaScript and non-course HTML.**

****如何在项目中包含三个. js？****

**在项目中添加 Three.js 的方法有很多，有些很简单，有些有点复杂，但是它们都表示我们必须在项目中包含这些文件中的任何一个:**

*   **三个。射流研究…**
**T3】three . min . jsT5】three . module . js**

**这些[所有的文件](https://github.com/mrdoob/three.js/tree/master/build)都可以在三. js 的 [GitHub 页面上找到。](https://github.com/mrdoob/three.js/tree/master)**

****方法 1:(下载完整的项目 Three.js):** 最简单的方法就是在你的系统上下载完整的 Three.js 项目，并从那里使用文件。**

**你可以从其 [GitHub 页面](https://github.com/mrdoob/three.js/tree/master)下载最新版本的 three.js。一旦你下载了它，打开它，看看里面的**建立**文件夹，你会发现那里的三个脚本。**

****方法 2:(使用 NPM 或纱安装三件套):**三件套在 NPM 上也有[套装。这意味着，如果您在计算机上设置了 Node.js 和 NPM，那么您可以打开命令提示符并键入:](https://www.npmjs.com/package/three)**

```
[npm i three](https://www.npmjs.com/package/three)
```

**然后，您可以通过引用三个包将三个. js 从三个. module.js 文件导入到您的 JavaScript 文件中:**

```
import * as THREE from "three";
```

**而且，如果你更喜欢纱线而不是 NPM，那么你也可以在终端窗口中使用以下命令添加包:**

```
yarn add three
```

****方法 3:(使用 CDN 链接):**您可以从 CDN(内容交付网络)链接文件，CDN 是一个专门托管文件的远程站点，因此您可以在网站中使用它们。**

**事实上，你甚至可以使用 Three.js.org 网站作为 CDN。您可以使用以下链接链接三. js 文件:[https://threejs.org/build/three.js](https://threejs.org/build/three.js)，并将其包含在您的 HTML 中，如下所示:**

```
<script src="https://threejs.org/build/three.js"></script>
```

**但是使用 three.js.org CDN 链接有一个问题，通过使用这个链接，你将总是在一个更新的版本上工作。当我们处于开发模式时，这很好，但如果我们谈论生产，这就不好了，如果任何功能或语法随着更新而改变，您的代码将停止工作，因此我们建议从以下网站使用 CDN:**

*   **[【cdnjs.com】](https://cdnjs.com/libraries/three.js/)**
*   **[www . jsdelivr . com](https://www.jsdelivr.com/package/npm/three)**

**就是这样，通过使用这些方法，你可以在你的项目中使用 [Three.js](https://threejs.org/) 。**