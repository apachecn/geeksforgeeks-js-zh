# tensorflow . js TF . metrics . cosineproximity()函数

> 原文:[https://www . geeksforgeeks . org/tensorflow-js-TF-metrics-cosineproximity-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-metrics-cosineproximity-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**TF . metrics . cosineproximity()**函数定义为:*--(L2 normalize(tensor 1))*(L2 normalize(tensor 2)))]*，其中 *l2Normalize()* 将输入的 L2 范数归一化为 1，并且*表示乘法。

**语法:**

```
tf.metrics.cosineProximity(yTrue, yPred)
```

**参数:**该函数接受以下两个参数:

*   **yTrue:** 是一个简单的真张量。
*   **yPred:** 是一个简单的预测张量。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing truth tensor.
let tensor1 = tf.tensor1d([1, 2, 3]);

// Initializing Prediction tensor.
let tensor2 = tf.tensor1d([
    Math.atan(8 / 10),
    Math.atan(4 / 5),
    Math.acosh(2)
]);

// Finding the result using .cosineProximity() Function
let result = tf.metrics.cosineProximity(tensor1, tensor2);

// Printing the result.
result.print();
```

**输出:**

```
Tensor
    -0.9819149971008301
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Finding the cosime proximity between
// truth and prediction tensor
// using .cosineProximity() Function
tf.metrics.cosineProximity(
    tf.tensor1d([1, 2, 3]),
    tf.tensor1d([4, 5, 6])
)
   .print();
```

**输出:**

```
Tensor
    -0.9746317863464355
```

**参考:**[https://js . tensorflow . org/API/3 . 6 . 0/# metrics . cosineproximity](https://js.tensorflow.org/api/3.6.0/#metrics.cosineProximity)