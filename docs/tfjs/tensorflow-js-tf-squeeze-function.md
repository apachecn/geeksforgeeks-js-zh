# tensorflow . js TF . crush()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-crush-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-squeeze-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。挤压()功能**用于将长度为 1 的尺寸从规定的张量形状中剔除

**语法:**

```
tf.squeeze(x, axis?)
```

**参数:**

*   **x:** 是所述的要被压缩的张量输入，可以是 tf 类型。张量、类型或数组。
*   **轴:**它是一个持有数字列表的可选参数。它只挤压规定的尺寸，以防其被指定。此外，这里的维度索引从零开始，压缩长度不是 1 的维度是一个缺陷。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor([11, 76, -4, 6], [2, 2, 1]);

// Calling squeeze() method and
// Printing output
y.squeeze().print();
```

**输出:**

```
Tensor
    [[11, 76],
     [-4, 6 ]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling squeeze() method with
// all its parameter
var res = tf.squeeze(tf.tensor(
    [2.1, 5.6, 8.6, 7.6], 
    [4, 1]), [1]
);

// Printing output
res.print();
```

**输出:**

```
Tensor
    [2.0999999, 5.5999999, 8.6000004, 7.5999999]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#squeeze