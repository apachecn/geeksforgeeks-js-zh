# tensorflow . js . TF . reverse()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-reverse-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-reverse-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf.stack()函数**用于沿特定轴反转 tf.tensors。

**语法:**

```
tf.stack (x, axis)
```

**参数:**

*   **x:** 要反转的输入张量。
*   **轴:**要设置的尺寸组。

**返回值:**这个函数返回 tf.Tensor

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a tensor
const gfg = tf.tensor1d([4, 3, 2, 1]);

// Printing tensor
gfg.reverse().print();
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

// Creating a tensor
const x = tf.tensor2d([2, 1, 4, 3, 6, 5], [3, 2]);

// Initialize the axis
const axis = 1;

// Printing the tensor
x.reverse(axis).print();
```

**输出:**

```
Tensor
    [[1, 2],
     [3, 4],
     [5, 6]]
```

**参考:**[https://js.tensorflow.org/api/latest/#reverse](https://js.tensorflow.org/api/latest/#reverse)