# tensorlow . js TF . pad()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-pad-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-pad-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf.pad()功能**用于填充 tf。带有给定值的张量和填充。

**语法:**

```
tf.pad(tensor, paddings, constantValue)
```

**参数:**该功能接受以下三个参数:

*   **张量:**是一个要垫的张量。
*   **填充:**它是一个长度为 R 的数组，R 是给定张量的秩，其中每个元素的长度为 int 的 2([pad _ Before，pad_After])，指定应该沿着张量的每个维度给定多少填充。
*   **常量值:**是要使用的填充值。默认值为 0。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing 3d tensor and then using
// .pad() function to print the result
tf.tensor3d([1, 2, 3, 4], [2, 2, 1])
  .pad([[0, 0], [1, 1], [2, 2]])
      .print();
```

**输出:**

```
Tensor
    [[[0, 0, 0, 0, 0],
      [0, 0, 1, 0, 0],
      [0, 0, 2, 0, 0],
      [0, 0, 0, 0, 0]],

     [[0, 0, 0, 0, 0],
      [0, 0, 3, 0, 0],
      [0, 0, 4, 0, 0],
      [0, 0, 0, 0, 0]]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing 2d tensor
let geek1 = tf.tensor2d([[1, 2], [3, 4]]);

// Using .pad() function.
let geek2 = geek1.pad([[0, 1], [2, 1]]);

// Printing the result.
geek2.print();
```

**输出:**

```
Tensor
    [[0, 0, 1, 2, 0],
     [0, 0, 3, 4, 0],
     [0, 0, 0, 0, 0]]
```

**参考资料:**[https://js . tensorlow . org/API/3 . 6 . 0/# pad](https://js.tensorflow.org/api/3.6.0/#pad)