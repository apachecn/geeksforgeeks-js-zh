# tensorflow . js TF . metrics .categoricalcross 熵()函数

> 原文:[https://www . geeksforgeeks . org/tensorflow-js-TF-metrics-categoricalcross 熵-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-metrics-categoricalcrossentropy-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

函数明确地找到目标和输出张量之间的分类交叉熵。

**语法:**

```
tf.metrics.categoricalCrossentropy(yTrue, yPred)
```

**参数:**该函数接受以下两个参数:

*   **yTrue:** 是真张量，是 tf.Tensor 类型。
*   **yPred:** 为预测张量，类型为 tf.Tensor。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initialising first 2d tensor.
let geek1 = tf.tensor2d([[2, 4], [1, 3]]);

// Initialising second 2d tensor.
let geek2 = tf.tensor2d([11, 22, 33, 44], [2, 2]);

// Using .categoricalCrossentropy() function
// to find categorical accuracy metric.
let result = tf.metrics.categoricalCrossentropy(geek1, geek2);

// Printing the result.
result.print();
```

**输出:**

```
Tensor
    [3.8190854, 2.526145]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using .categoricalCrossentropy() function
// to find categorical accuracy metric
tf.metrics.categoricalCrossentropy(
  tf.tensor1d([1, 2]), 
   tf.tensor2d([50], [1, 1]))
      .print();
```

**输出:**

```
Tensor
    [4e-7]
```

**参考:**[https://js . tensorflow . org/API/3 . 6 . 0/# metrics .categoricalcross 熵](https://js.tensorflow.org/api/3.6.0/#metrics.categoricalCrossentropy)