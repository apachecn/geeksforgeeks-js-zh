# tensorflow . js TF . metrics . sparsecategoricalocracy()函数

> 原文:[https://www . geeksforgeeks . org/tensorflow-js-TF-metrics-sparecategoriaccucracy-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-metrics-sparsecategoricalaccuracy-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

函数是一个稀疏分类精度度量函数，它使用索引和逻辑来返回 tf。张量对象。

**语法:**

```
tf.metrics.sparseCategoricalAccuracy(yTrue, yPred) 
```

**参数:**

*   **yTrue:** 它是所述的真实标签，即*指数*，并且它可以是 tf.Tensor 类型
*   **yPred:** 是预测的期望或逻辑，可以是 tf.Tensor 类型

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining indices and logits
const y = tf.tensor1d([1, 2, 1, 7]);
const z = tf.tensor2d([[1, 1, 9], [0.2, 0, 1], [0.1], [1.8]]);

// Calling metrics.sparseCategoricalAccuracy() 
// method
const sparseCategoricalAccuracy = 
    tf.metrics.sparseCategoricalAccuracy(y, z);

// Printing output
sparseCategoricalAccuracy.print();
```

**输出:**

```
Tensor
    [0, 1, 1, 0]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling metrics.sparseCategoricalAccuracy()
// method and printing output
tf.metrics.sparseCategoricalAccuracy(
    tf.tensor1d([2, 3, null, 'a']), 
    tf.tensor2d([[0, 0, 0], [0, 0, 1], 
    [2, 2, 2], [6, 7, 8]])
).print();
```

**输出:**

```
Tensor
    [0, 0, 1, 0]
```

**参考:**T2