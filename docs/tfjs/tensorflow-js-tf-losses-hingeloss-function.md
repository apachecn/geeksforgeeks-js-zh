# tensorflow . js . TF . loss . hinge loss()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-loss-hinge loss-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-losses-hingeloss-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

函数计算两个给定张量之间的铰链损耗。

**语法:**

```
tf.losses.hingeLoss (labels, predictions, weights, reduction)
```

**参数:**

*   **标签:**指定真值输出张量。基于这个张量预测绝对差。
*   **预测:**指定预测输出张量，维度与标签相同。
*   **权重:**它指定等级张量等于标签的等级张量，因此它可以是可展宽的或 0。这是一个可选参数。
*   **减少:**规定了减少损失的类型。这是一个可选参数。

**返回值:**返回一个 tf。由 hingeLoss()函数计算的张量。

**示例 1:** 在本例中，我们将使用两个 2d 张量作为标签和预测。然后我们将找到这两个张量之间的估计铰链损耗。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs");

// Defining label tensor
const x_label = tf.tensor2d([
    [0., 1., 0.], 
    [1., 0., 1.]
]);

// Defining prediction tensor
const x_pred = tf.tensor2d([
    [1., 1., 1.], 
    [0., 0., 0\. ]
]);

// Calculating hinge loss
const hinge_loss = tf.losses.hingeLoss(x_label,x_pred)

// Printing the output
hinge_loss.print()
```

**输出:**

```
Tensor
    1.1666667461395264
```

**例二:**

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Computing hinge loss between two
// tensors and printing the result
tf.losses.hingeLoss(
    tf.tensor4d([[[[0], [4]], [[5], [1]]]]),
    tf.tensor4d([[[[1], [2]], [[3], [4]]]])
).print();
```

**输出:**

```
Tensor
    0.5
```

**参考:**[**https://js.tensorflow.org/api/1.0.0/#losses.hingeLoss**](https://js.tensorflow.org/api/latest/#losses.hingeLoss)