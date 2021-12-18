# tensorflow . js TF . one like()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-one like-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-oneslike-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**TF . one like()**函数用于创建 **tf。张量**所有元素设置为 1，形状与给定的张量相同。

**语法:**

```
tf.onesLike (x)
```

**参数:**

*   **x:** a tf。其所有元素将被设置为 1 的张量。

**返回值:**返回一个 tf.Tensor

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor
const x = tf.tensor([1, 2]);

// Printing the tensor after setting the value of tensor to 1
tf.onesLike(x).print();
```

**输出:**

```
Tensor
   [1, 1]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor
const x = tf.tensor2d([8, 2, 5, 6], [2, 2]);

// Printing the tensor after setting the value of tensor to 1
tf.onesLike(x).print();
```

**输出:**

```
Tensor
   [[1, 1],
    [1, 1]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#onesLike