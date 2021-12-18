# Tensorflow.js tf .多项式()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-多项式-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-multinomial-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。多项式()函数**用于生成一个 tf。张量以及从多项式分布中拉出的输入。

**语法:**

```
tf.multinomial(logits, numSamples, seed?, normalized?)
```

**参数:**

*   **逻辑:**它是一个陈述的 1D 数组和无组织的对数期望，或者是一个 2D 数组，它有一个形状【batchSize，numOutcomes】，它可以是 tf 类型。张量 1D，tf。张量 2D、TypedArray 或数组。
*   **数量样本:**是为每个行部分拖动的样本的规定数量。它是数字类型的。
*   **种子:**是规定的种子号，是类型号的可选参数。
*   **归一化:**它检查给定的逻辑是否有真正的预期(即总和为 1)。默认值为 false，是布尔类型的可选参数。

**返回值:**返回 tf。张量 1D，或 tf .张量 2D

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining logits
const logits = tf.tensor([35, 158]);

// Calling tf.multinomial() method and
// Printing output
tf.multinomial(logits, 4).print();
```

**输出:**

```
Tensor
    [1, 1, 1, 1]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling tf.multinomial() method and
// Printing output
tf.multinomial(tf.tensor(
  [5.7, 8.7, NaN, 'a', null, 0]), 6).print();
```

**输出:**

```
Tensor
    [5, 5, 5, 5, 5, 5]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#multinomial