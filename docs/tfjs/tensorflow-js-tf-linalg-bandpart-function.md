# tensorflow . js TF . linalg . band part()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-linalg-band part-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-linalg-bandpart-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf.linalg.bandPart()** 函数用于计算给定张量的带部分。

**语法** :

```
tf.linalg.bandPart (a, numLower, numUpper)
```

**参数:**

*   **a:** 传递的是 tf.tensor。
*   **numLower:** 要保留的子对角线数量。如果为负，保留整个下三角形
*   **numipper:**要保留的子段数。如果为负，保留整个上三角形

**返回值**:返回 tf.Tensor1D

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

const x = tf.tensor2d([[ 0,  1,  2, 3],
                     [ 4,  0,  1, 2],
                     [ 3,  1,  0, 1],
                     [ 3,  1,  1, 0]]);

let y = tf.linalg.bandPart(x, 1, 3);
y.print();
```

**输出:**

```
Tensor
   [[0, 1, 2, 3],
    [4, 0, 1, 2],
    [0, 1, 0, 1],
    [0, 0, 1, 0]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

const x = tf.tensor2d([[ 0,  1,  2, 3],
                     [ 4,  0,  1, 2],
                     [ 3,  1,  0, 1],
                     [ 3,  1,  1, 0]]);

let k = tf.linalg.bandPart(x, -1, -3);
k.print();
```

**输出:**

```
Tensor
   [[0, 1, 2, 3],
    [4, 0, 1, 2],
    [3, 1, 0, 1],
    [3, 1, 1, 0]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#linalg.bandPart