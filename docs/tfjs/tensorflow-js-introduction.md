# tensorlow . js introduction

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-introduction/

#### 什么是 Tensorflow.js？

[TensorFlow.js](https://www.tensorflow.org/js/tutorials) 是一个 JavaScript 库，用于在 web 应用程序和 Node.js 中训练和部署机器学习模型，您可以使用 TensorFlow.js 从头开始开发机器学习模型，也可以使用提供的 API 在浏览器或 Node.js 服务器上训练您现有的模型。

要了解更多信息，您可以直接访问以下链接:https://www . tensorflow . org/resources/learn-ml/basic of-tensorflow-for-js-development。

**先决条件:**在启动 Tensorflow.js 之前，您需要了解以下内容:

**浏览器:**

*   超文本标记语言:需要超文本标记语言的基础知识
*   JavaScript:需要良好的 JS 知识

**服务器端:**

*   同时，由于 Node.js 是一个 js 运行时，所以在 JavaScript 上有命令会有很大的帮助。

**其他要求:**

*   NPM 或纱:这些是需要安装在您的系统中的软件包。

**设置张量流:**

**浏览器设置**在基于浏览器的应用程序中，有两种方法可以添加 TensorFlow.js:

*   使用脚本标签。
*   从 NPM 安装

**1。使用脚本标签:**将以下脚本标签添加到您的主 HTML 文件中。

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <script src=
"https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@2.0.0/dist/tf.min.js">
    </script>
</head>

<body>
    <script>

        // Value of a scalar
        var value = "Hello Geeks! Tensorflow here."

        // Creating the value of a scalar
        var tens = tf.scalar(value)

        document.write(tens)
    </script>
</body>

</html>
```

输出:

![](img/23a7a48238bf27acf574ef82888fd3d7.png)

**2。使用 NPM/纱线:**我们可以使用 NPM 或纱线来安装 tensorflow.js。

```
yarn add @tensorflow/tfjs
```

或者

```
npm install @tensorflow/tfjs
```

**节点 js 设置:**

**选项 1:** 用本机 C++绑定安装 TensorFlow.js。

```
yarn add @tensorflow/tfjs-node
```

或者

```
npm install @tensorflow/tfjs-node
```

**选项 2:** (仅适用于 Linux)如果您的系统具有支持 CUDA 的 NVIDIA GPU，请使用 GPU 包以获得更高的性能。

```
yarn add @tensorflow/tfjs-node-gpu
```

或者

```
npm install @tensorflow/tfjs-node-gpu
```

**选项 3:** 安装纯 JavaScript 版本。就性能而言，这是最慢的选项。

```
yarn add @tensorflow/tfjs
```

或者

```
npm install @tensorflow/tfjs
```