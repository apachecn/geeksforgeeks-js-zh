# Tensorflow.js tf。张量类。数据同步()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-tensor-class-datasync-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-class-datasync-method/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf。张量类。dataSync()** 方法用于同步下载 tf.Tensor 中的值

**语法:**

```
dataSync()
```

**参数:**

*   它不需要参数

**返回值:**返回数据类型映射[数值数据类型]

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

console.log(tf.tensor([1, 3, 5, 4, 2]).dataSync())
```

**输出:**

```
1, 3, 5, 4, 2
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

const a= tf.tensor2d([[0, 1], [2, 3]])
console.log(a.dataSync())
```

**输出:**

```
0, 1, 2, 3
```

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.Tensor.dataSync