# Tensorflow.js tf.topk()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-topk-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-topk-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**tf.topk()** 函数和最后一个维度也用于查找 k 个最大条目的值和索引。

**语法:**

```
tf.topk (x, k?, sorted?)
```

**参数:**

*   **x:** 1-D 或更高的 tf。最后维度至少为 k 的张量。
*   **k:** 是要找的元素个数。
*   **排序:**为布尔值。如果是真的，那么得到的 k 个元素将按值降序排序。

**返回值:**{值:tf。张量，指数:tf。张量}。它返回一个带有两个张量的对象，这两个张量包含值和索引。

**例 1:**

## Javascript

```
const tf = require("@tensorflow/tfjs")

// Creating a 2d tensor
const a = tf.tensor2d([[1, 20, 3], [4, 3, 1], [8, 9, 10]]);
const {values, indices} = tf.topk(a);

// Printing the values and indices
values.print();
indices.print();
```

**输出:**

```
Tensor
    [[20],
     [4 ],
     [10]]
Tensor
    [[1],
     [0],
     [2]]
```

**示例 2:** 在本例中，我们将提供参数 k，以获得最大的 k 个条目。

## Javascript

```
const tf = require("@tensorflow/tfjs")

// Creating a 2d tensor
const a = tf.tensor2d([[1, 20, 3], [4, 3, 1], [8, 9, 10]]);
const {values, indices} = tf.topk(a, 3);

// Printing the values and indices
values.print();
indices.print();
```

**输出:**

当我们通过 k = 3 时，我们得到结果中的 3 个最大值。

```
Tensor
    [[20, 3, 1],
     [4 , 3, 1],
     [10, 9, 8]]
Tensor
    [[1, 2, 0],
     [0, 1, 2],
     [2, 1, 0]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#topk