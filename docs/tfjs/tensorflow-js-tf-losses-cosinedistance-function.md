# tensorflow . js TF . loss . cosinedistance()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-loss-cosine distance-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-losses-cosinedistance-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**函数用于计算两个张量之间的余弦距离损失。**

**语法:**

```
tf.losses.cosineDistance(labels, predictions, 
        axis, weights?, reduction?) 
```

**参数:**该函数接受五个参数，其中最后两个是可选的，如下图所示:

*   **标签:**地面真值输出张量。维度将与预测相同。
*   **预测:**预测输出。
*   **轴:**余弦距离是沿着这个维度计算的。
*   **权重:**它是一个秩为 0 的张量，或者与标签具有相同的秩，并且它必须可扩展到标签，这意味着所有维度必须是 1，或者与相应的损失维度相同。此参数是可选的。
*   **减少:**适用于损失的减少类型。这也是一个可选参数。

**返回值:**它返回一个张量，这是两个张量之间的余弦距离损失。

**例 1:**

## java 描述语言

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Creating labels tensor
const a = tf.tensor2d([[1, 4, 5], [5, 5, 7]]);

// Creating predictions tensor
const b = tf.tensor2d([[3, 2, 5], [3, 2, 7]])

// Computing cosine distance
cosine = tf.losses.cosineDistance(a, b)
cosine.print();
```

**输出:**

```
Tensor
    -109
```

**示例 2:** 在本例中，我们将传递一个额外的参数，即权重。这是一个可选参数。

## java 描述语言

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Creating labels tensor
const a = tf.tensor2d([
    [1, 4, 5, 5, 5, 7],
    [4, 7, 6, 8, 9, 4]
]);

// Creating predictions tensor
const b = tf.tensor2d([
    [3, 2, 5, 3, 2, 7],
    [3, 5, 7, 2, 4, 5]
]);

// Computing cosine distance
cosine = tf.losses.cosineDistance(a, b , 1)
cosine.print();
```

**输出:**

```
Tensor
   -134.5
```

**参考:**T2https://js.tensorflow.org/api/latest/#losses.cosineDistance