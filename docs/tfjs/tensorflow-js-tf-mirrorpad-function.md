# tensorlow . js TF . mirrorpad()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-mirrorpad-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-mirrorpad-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。mirrorPad()功能**用于借助镜像填充来填充所述张量输入。此外，该方法有利于实现 pad 的*反射*和*对称*模式。

**语法:**

```
tf.mirrorPad(x, paddings, mode)
```

**参数:**

*   **x:** 是要填充的陈述张量，可以是 tf 类型。张量、类型或数组。
*   **划水:**它是一个长度为 *R 的数组，*是所述张量的阶。其中，所有元素形成长度为 2 的元组，即 ints [padBefore，padAfter]，指定用所述张量的每个大小填充到什么程度。此外，在*反射*填充模式中，填充部分应排除末端，而在*对称*填充模式中，填充部分不应排除末端。它属于数组类型。
*   **模式:**指定填充模式，即要么*反射*要么*对称*。它是字符串类型的。

**注:**

*   首先，如果所述张量输入是[4，5，6]并且填充是[0，1]，那么输出将是在*中的[4，5，6，5]反映填充的*模式和在*对称的*填充的【4，5，6，6】模式。
*   其次，如果填充模式为*反射*，则填充[D，0]以及填充[D，1]不得高于 x 形状[D]–1，而如果填充模式为*对称*，则填充[D，0]以及填充[D，1]不得高于 x 形状[D]。

**返回值:**返回 tf。张量对象。

**例 1:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input
const y = tf.tensor1d([4, 5, 6]);

// Defining paddings and mode of
// padding
const padding = [[0, 1]];
const mode = 'reflect';

// Calling tf.mirrorPad() method
var res = tf.mirrorPad(y, padding, mode);

// Printing output
res.print();
```

**输出:**

```
Tensor
    [4, 5, 6, 5] 
```

**例 2:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling tf.mirrorPad() method and
// Printing output
tf.mirrorPad(tf.tensor(
    [2.4, 6.8, 9.3, 5.3]),
    [[0, 2]], 'symmetric').print();
```

**输出:**

```
Tensor
    [2.4000001, 6.8000002, 9.3000002, 
    5.3000002, 5.3000002, 9.3000002] 
```

**参考:**T2】https://js.tensorflow.org/api/latest/#mirrorPad