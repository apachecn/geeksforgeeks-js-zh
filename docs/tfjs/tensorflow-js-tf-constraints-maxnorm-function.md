# tensorflow . js TF . constraints . maxnorm()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-constraints-max norm-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-constraints-maxnorm-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。
TF . constraints . MaxNorm()是从约束类继承的。约束是层的属性，如权重、核、偏差。它在模型构建时分配给层。MaxNorm 是一个权重约束。它将权重限制为每个隐藏层的范数小于或等于期望值。在这篇文章中，我们将看到 maxNorm()函数以及它如何在约束条件下工作。

**语法:**

```
tf.constraints.maxNorm(maxValue, axis) 
```

**参数:**

*   **最大值:**入库重量的最大定额。
*   **轴:**是计算范数的轴。

**返回:**返回 tf.constraints.Constraint。

**示例 1:** 在本例中，我们将创建 maxNorm 函数，并将 maxValue 作为 2 传递，将 axis 作为 0 传递。

## java 描述语言

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Use maxNorm() function
var a=tf.constraints.maxNorm(2,0)

// Print
console.log(a)
```

**输出:**

```
{
    "defaultMaxValue": 2,
    "defaultAxis": 0,
    "maxValue": 2,
    "axis": 0
}
```

**示例 2:** 在本例中，我们将创建一个密集层的模型，并将内核和偏差约束作为 maxNorm 传递。

## java 描述语言

```
// Import tensorflow.js
import * as tf from "@tensorflow/tfjs"

// Define dense layer
const denseLayer = tf.layers.dense({
    units: 6,
    kernelInitializer: 'heNormal',
    kernelConstraint: 'maxNorm',
    biasConstraint: 'maxNorm',
    useBias: true
});

// Define input and output
const inp = tf.ones([2, 3]);
const out = denseLayer.apply(inp);

// Print the output
out.print()
```

**输出:**

```
Tensor
   [[0.770891, -0.191616, -1.3709277, -1.010246, 1.0177934, 0.6692461],
    [0.770891, -0.191616, -1.3709277, -1.010246, 1.0177934, 0.6692461]]
```

**参考:**[https://js.tensorflow.org/api/latest/#class:constraints.约束](https://js.tensorflow.org/api/latest/#class:constraints.Constraint)