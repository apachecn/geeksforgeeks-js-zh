# Tensorflow.js tf.slice()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-slice-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-slice-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf.slice()函数**用于从 tf 中提取一个切片。张量从坐标“begin”开始，大小为“size”。

**语法:**

```
tf.slice (x, begin, size?)
```

**参数:**

*   **x:** 将输入张量转为切片形式。
*   **开始:**开始切片的坐标。
*   **大小:**切片的大小

**返回值:**返回 tf.Tensor

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"
const x = tf.tensor1d([1, 2, 3, 4, 5, 6, 7]);

x.slice([0], [4]).print();
```

**输出:**

```
Tensor
    [1, 2, 3, 4]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"
const x = tf.tensor2d([1, 2, 3, 4, 5, 6], [2, 3]);

x.slice([1, 0], [1, 2]).print();
```

**输出:**

```
Tensor
     [1,2,3,4]
```

**参考:**[https://js.tensorflow.org/api/latest/#slice](https://js.tensorflow.org/api/latest/#slice)