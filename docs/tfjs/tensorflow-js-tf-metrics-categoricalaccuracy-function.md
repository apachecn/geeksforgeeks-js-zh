# tensorflow . js TF . metrics . categoricalocracy()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-metrics-categoricalaccuracy-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-metrics-categoricalaccuracy-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**TF . metrics . categoricalocracy()**函数用于返回两个张量之间的分类精度。它以两个张量为参数。

**语法:**

```
tf.metrics.categoricalAccuracy(a, b);
```

**参数:**

*   **a:** 第一个指定张量。
*   **b:** 第二个指定张量。它必须具有与**【a】相同的数据类型。**

****返回值:**返回两个指定张量“a”和“b”的分类精度。**

****例 1:****

## **Javascript**

```
// Importing the tensorflow library
import * as tf from "@tensorflow/tfjs"

// Initializing two tensors
const a = tf.tensor2d([[1, 0, 0, 1], [0, 1, 0, 1]]);
const b = tf.tensor2d([
    [0.1, 0.6, 0.01, 0.05], 
    [0.1, 0.02, 0.05, 0.3]
]);

// Calling the .categoricalAccuracy() function
const accuracy = tf.metrics.categoricalAccuracy(a, b);

// Print tensor 
accuracy.print();
```

****输出:****

```
Tensor
    [0, 0]
```

****例二:****

## **Javascript**

```
// Importing the tensorflow library
import * as tf from "@tensorflow/tfjs"

// Initializing two tensors
const a = tf.tensor([1, 0, 0, 1]);
const b = tf.tensor([1, 0.6, 0.01, 0.05]);

// Calling the .categoricalAccuracy() function
const accuracy = tf.metrics.categoricalAccuracy(a, b);

// Print tensor 
accuracy.print();
```

****输出:****

```
Tensor
    1
```

****例三:****

## **Javascript**

```
// Importing the tensorflow library
import * as tf from "@tensorflow/tfjs"

// Initializing two tensors
const a = tf.tensor([0, 0, 0, 1]);
const b = tf.tensor([0.1, 0.8, 0.05, 0.05]);

// Calling the .categoricalAccuracy() function
const accuracy = tf.metrics.categoricalAccuracy(a, b);

// Print tensor 
accuracy.print();
```

****输出:****

```
Tensor
    0
```

****参考:**T2**