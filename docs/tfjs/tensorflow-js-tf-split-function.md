# Tensorflow.js tf.split()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-split-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-split-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf.split()函数**用于将 tf.tensorss 拆分为子 tensor。

**语法:**

```
tf.split (x, numOrSizeSplits, axis?)
```

**参数:**

*   **x:** 要拆分的输入张量。
*   **numOrSizeSplits:** 它可以是表示分割数量的数字，也可以是为每个输出张量提供大小的数组
*   **轴:**是要沿其拆分的维度的轴。

**返回值:**返回 tf。张量[]。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

const x = tf.tensor2d([10, 20, 50, 60,
                       30, 40, 70, 80], [2, 4]);

// Split the tensor
const [gfg, geeks] = tf.split(x, 2, 1);

gfg.print();

geeks.print();
```

**输出:**

```
Tensor
    [[10, 20],
     [30, 40]]
Tensor
    [[50, 60],
     [70, 80]]
```

**示例 2:** 在本例中，将轴作为第二个参数的分割作为一个数组。

## Javascript

```
const x = tf.tensor2d([10, 30, 50, 70, 20, 40, 60, 80], [2, 4]);

const [gfg, gfg1, geeks] = tf.split(x, [1, 2, 1], 1);

gfg.print();

gfg1.print();

geeks.print();
```

**输出:**

```
Tensor
    [[10],
     [20]]
Tensor
    [[30, 50],
     [40, 60]]
Tensor
    [[70],
     [80]]
```

**参考:**[https://js.tensorflow.org/api/latest/#split](https://js.tensorflow.org/api/latest/#split)