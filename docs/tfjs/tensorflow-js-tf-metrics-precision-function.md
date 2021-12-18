# tensorflow . js TF . metrics . precision()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-metrics-precision-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-metrics-precision-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**.metrics.precision()函数**用于参照名称计算期望的精度。

**语法:**

```
tf.metrics.precision(yTrue, yPred)
```

**参数:**

*   **yTrue:** 它是所陈述的地面真张量，它应该保存从 0 到 1 的值，并且它可以是 tf.Tensor 类型
*   **yPred:** 它是所述的预测张量，假设它保存从 0 到 1 的值，并且它可以是 tf.Tensor 类型

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining truth and prediction tensors
const y = tf.tensor2d([[0, 1], [1, 1]]);
const z = tf.tensor2d([[1, 0], [0, 1]]);

// Calling metrics.precision() method
const pre = tf.metrics.precision(y, z);

// Printing output
pre.print();
```

**输出:**

```
Tensor
    0.5
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling metrics.precision() method with
// its parameter directly and then 
// Printing output
const output = tf.metrics.precision(tf.tensor(
    [
      [0, 1, 0, 0],
      [0, 1, 1, 0],
      [0, 0, 0, 1],
      [1, 1, 0, 0],
      [0, 0, 1, 0]
    ]
), tf.tensor(
    [
      [0, 0, 1, 1],
      [0, 1, 1, 0],
      [0, 0, 0, 1],
      [0, 1, 0, 1],
      [1, 1, 0, 0]
    ]
)).print();
```

**输出:**

```
Tensor
    0.4444444477558136
```

**参考:**T2】https://js.tensorflow.org/api/latest/#metrics.precision