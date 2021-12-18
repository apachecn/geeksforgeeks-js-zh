# 张量流.js tf.argMax（） 函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-arg max-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-argmax-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.argMax()** 函数用于返回指定张量沿轴的最大值的索引。

输出结果具有与输入相同的形状，沿轴的尺寸被移除。

**语法:**

```
tf.argMax (x, axis)
```

**参数:**该函数接受两个参数，如下图所示:

*   **x:** Enter the tensor.
*   **Axis:** The specified size to be reduced. It is an optional parameter with a default value of 0.

**返回值:**它返回沿轴的最大值的指数张量。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a some tensors 
const a = tf.tensor1d([1, 0]);
const b = tf.tensor1d([3, 5]);
const c = tf.tensor1d([6, 3, 5, 12]);

// Calling the .argMax() function over 
// the above tensors
a.argMax().print();
b.argMax().print();
c.argMax().print();
```

**输出:**

```
Tensor
   0
Tensor
   1
Tensor
   3
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a some tensors 
const a = tf.tensor1d([0, 1]);
const b = tf.tensor2d([9, 5, 2, 8], [2, 2]);
const c = tf.tensor1d([6, 4, 7]);

// Initializing a axis parameters
const axis1 = -1;
const axis2 = -2;
const axis3 = 0;

// Calling the .argMax() function over 
// the above tensors
a.argMax(axis1).print();
b.argMax(axis2).print();
c.argMax(axis3).print();
```

**输出:**

```
Tensor
   1
Tensor
   [0, 1]
Tensor
   2
```

**参考:**T2】https://js.tensorflow.org/api/latest/#argMax