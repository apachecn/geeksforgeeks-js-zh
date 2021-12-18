# tensorflow . js TF . constraints . minmax norm()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-constraints-minmax norm-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-constraints-minmaxnorm-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**TF . constraints . minMaxNorm()**函数用于基于给定的*配置*对象创建一个 minmax norm 约束。它继承自约束类。约束是层的属性，如权重、核、偏差。minMaxNorm 是一个权重约束。

**语法:**

```
tf.constraints.minMaxNorm(config)
```

**参数:**该函数将*配置*对象作为参数，该参数可以具有以下属性:

*   **最大值:**指定入库重量的最大定额。
*   **混合值:**它指定了传入重量的最小标准。
*   **轴:**指定计算范数所沿的轴。
*   **速率:**指定强制约束的速率。

**返回值:**返回一个 tf.constraints.Constraint。

**例 1:**

## java 描述语言

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Use maxNorm() function
const constraint = tf.constraints.minMaxNorm(1,0)

// Print the output
console.log(constraint)
```

**输出:**

```
{
  "defaultMinValue": 0,
  "defaultMaxValue": 1,
  "defaultRate": 1,
  "defaultAxis": 0,
  "minValue": 0,
  "maxValue": 1,
  "rate": 1,
  "axis": 0
}
```

**示例 2:** 在本例中，我们将使用 minMaxNorm 约束创建一个密集层。

## java 描述语言

```
// Import tensorflow.js
import * as tf from "@tensorflow/tfjs"

// Create a new dense layer using
// minMaxNorm constraint
const denseLayer = tf.layers.dense({
    units: 4,
    kernelInitializer: 'heNormal',
    kernelConstraint: 'minMaxNorm',
    biasConstraint: 'minMaxNorm',
    useBias: true
});

// Create input and output tensors
const input = tf.ones([2, 2]);
const output = denseLayer.apply(input);

// Print the output
output.print()
```

**输出:**

```
Tensor
    [[1.5594537, 0.1787095, 0.3462192, -1.7434707],
     [1.5594537, 0.1787095, 0.3462192, -1.7434707]]
```

**参考:**T2】https://js.tensorflow.org/api/1.0.0/#constraints.minMaxNorm