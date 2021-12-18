# Tensorflow.js tf.step()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-step-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-step-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.step()** 函数用于返回输入张量元素的步长，即如果元素大于 0 则返回 1，否则返回α，其中α是函数 step()的参数。

**语法:**

```
tf.step (x, alpha)
```

**参数:**该函数接受两个参数，如下图所示:

*   **x:** 指定的输入张量。
*   **α:**负输入值的梯度。

**返回值:**返回输入张量元素的步长。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a tensor of some elements
const x = tf.tensor1d([2, 0, -2, -5]);

// Calling the .step() function over
// the above tensor as its parameter and
// for the alpha value .2
x.step(.2).print();
```

**输出:**

```
Tensor
   [1, 0.2, 0.2, 0.2]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using a tensor of some elements as 
// the parameter for the .step() function with
// alpha value of 6
tf.tensor1d([0, .8, -1, -5.4]).step(6).print();
```

**输出:**

```
Tensor
   [6, 1, 6, 6]
```