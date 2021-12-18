# tensorflow . js TF . constraints . nonneg()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-constraints-nonneg-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-constraints-nonneg-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**tf.constraints.nonNeg()** 函数我们用来创建一个 nonNeg 约束。 **nonNeg** 是非负权重约束。它继承自约束类。约束是层的属性。

**语法:**

```
 tf.constraints.nonNeg() 
```

**参数:**

*   **w:** 指定输入权重变量。这是一个可选参数。

**返回值:**返回 tf.constraints.Constraint。

**例 1:**

## java 描述语言

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Use nonNeg() function
const constraint = tf.constraints.nonNeg( )

// Print
console.log(constraint)
```

**输出**

```
{}
```

**示例 2:** 在本例中，我们将使用 nonNeg 约束创建一个密集层，并将形成的层应用到张量。

## java 描述语言

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Create nonNeg constarint using nonNeg() function
const constraint = tf.constraints.nonNeg()

// Create a new dense layer using nonNeg constraint
const denseLayer = tf.layers.dense({
    units: 4,
    kernelInitializer: 'heNormal',
    kernelConstraint: constraint ,
    biasConstraint: constraint ,
    useBias: true
});

// Create input
const input = tf.ones([2, 2]);

// Apply denseLayer to input
const output = denseLayer.apply(input);

// Print the output
output.print()
```

**输出**

```
Tensor
    [[-0.7439224, -1.3572885, -1.2860565, 1.3913929],
     [-0.7439224, -1.3572885, -1.2860565, 1.3913929]]
```

**参考:**T2】https://js.tensorflow.org/api/1.0.0/#constraints.nonNeg