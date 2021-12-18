# tensorflow . js TF . loss . computeweightdloss()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-loss-computeweighdloss-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-losses-computeweightedloss-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

函数的作用是:计算两个给定张量之间的加权损失。

**语法:**

```
tf.losses.computeWeightedLoss(losses, weights, reduction)
```

**参数:**

*   **损失:**是形状张量。
*   **重量:**这些是等级为 0 或 1 的张量，必须是宽可铸才能变形。
*   **还原:**适用于亏损的还原类型。它必须是缩减类型。

**注:***重量*、*减重*为可选参数。

**返回值:**返回 tf.Tensor。

**例 1:**

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Initialising tensor1 as geek1.
let geek1 = tf.tensor2d([[1, 2, 5], [6, 7, 10]]);

// Initialising tensor2 as geek2.
let geek2 = tf.tensor2d([[5, 7, 11], [2, 4, 8]])

//computing weight loss between geek1 and geek2.
geek = tf.losses.computeWeightedLoss(geek1, geek2)
geek.print();
```

**输出:**

```
Tensor
    32.333335876464844
```

**例二:**

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Computing weight loss between 3D and
// 4D tensors and printing the result.
tf.losses.computeWeightedLoss(
    tf.tensor3d([[[1], [2]], [[3], [4]]]),
    tf.tensor4d([[[[1], [2]], [[3], [4]]]])
).print();
```

**输出:**

```
Tensor
    7.5
```

**参考:**[**https://js . tensorflow . org/API/latest/# loss . computeweighdloss**](https://js.tensorflow.org/api/latest/#losses.computeWeightedLoss)