# tensorlow . js TF . sqrt()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sqrt-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-sqrt-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.sqrt()** 函数用于返回指定张量元素的平方根。

**语法:**

```
tf.sqrt( x )
```

**参数:**该函数接受单个参数，如下图所示:

*   **x:** 指定的输入张量。

**返回值:**返回指定张量元素的平方根。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a tensor of some elements
const x = tf.tensor1d([4, 9, 16, 25]);

// Calling the .sqrt() function over
// the above tensor as its parameter
x.sqrt().print();
```

**输出:**

```
Tensor
   [2, 3, 4, 5]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using a tensor of some elements
// as the parameter for the .sqrt() function
tf.tensor1d([0, 1, 2, 1.7, 2.5]).sqrt().print();
```

**输出:**

```
Tensor
   [0, 1, 1.4142135, 1.3038405, 1.5811388]
```