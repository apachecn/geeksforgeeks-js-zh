# tensorflow . js TF . constraints . unitnorm()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-constraints-unitnorm-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-constraints-unitnorm-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**TF . constraints . unitNorm()**函数我们用来创建一个 unitNorm()约束。它继承自约束类。约束用作创建**的属性。层。层。单位标准**约束约束作为此权重实例的每个隐藏单位具有单位标准。

**语法:**

```
tf.constraints.unitNorm(args) 
```

**参数:**

*   **参数:**指定包含配置的对象。
    1.  **轴:**指定计算范数所沿的轴。

**返回值:**返回 tf.constraints.Constraint。

**例 1:**

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Use unitNorm() function
const constraint = tf.constraints.unitNorm({axis :1})

// Print
console.log(constraint)
```

**输出**

```
{
  "defaultAxis": 0,
  "axis": 1
}
```

**示例 2:** 在本例中，我们将使用 unitNorm 约束创建一个密集层。

## Javascript

```
// Import tensorflow.js
import * as tf from "@tensorflow/tfjs"

// Create a new dense layer using unitNorm constraint
const denseLayer = tf.layers.dense({
    units: 4,
    kernelInitializer: 'heNormal',
    kernelConstraint: 'unitNorm',
    biasConstraint: 'unitNorm',
    useBias: true
});

// Create input tensor
const input = tf.ones([2, 2]);

// Apply dense layer to input tensor
const output = denseLayer.apply(input);

// Print the output
output.print()
```

**输出**

```
Tensor
    [[0.3154395, 0.3988628, 1.3295887, -0.0849797],
     [0.3154395, 0.3988628, 1.3295887, -0.0849797]]
```

**参考:**T2】https://js.tensorflow.org/api/1.0.0/#constraints.unitNorm