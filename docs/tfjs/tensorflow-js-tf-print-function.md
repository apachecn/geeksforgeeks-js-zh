# Tensorflow.js tf.print()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-print-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-print-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它帮助开发人员在 JavaScript 中开发 ML 模型，并直接在浏览器或 Node.js 中使用 ML。

**tf.print()** 功能用于打印关于 **tf.tensor** 及其数据的信息。

**语法:**

```
tf.print (x, verbose)
```

**参数:**

*   **x:** 要打印的张量
*   **verbose:** 是可选参数。这些是布尔参数，决定是否打印关于张量的详细信息，包括数据类型和大小。

**返回:**它不返回任何东西，即空。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Setting the value of verbose
const verbose = true;

// Creating the tensor
var val = tf.tensor2d([8, 2, 5, 6], [2, 2]);

// Printing the tensor
val.print(verbose)
```

**输出:**

```
Tensor
   dtype: float32
   rank: 2
   shape: [2,2]
   values:
      [[8, 2],
       [5, 6]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Setting the value of verbose
const verbose = false;

// Creating the tensor
var val = tf.tensor2d([8, 2, 5, 6], [2, 2]);

// Printing the tensor
val.print(verbose)
```

**输出:**

```
Tensor
   [[8, 2],
    [5, 6]]
```

**参考资料:**[https://js . tensorlow . org/API/3 . 4 . 0/# print](https://js.tensorflow.org/api/3.4.0/#print)