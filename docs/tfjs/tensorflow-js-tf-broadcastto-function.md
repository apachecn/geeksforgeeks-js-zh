# Tensorflow.js tf.broadcastTo()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-broad castto-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-broadcastto-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。broadcastTo()函数**用于将数组循环到 NumPy 风格的一致模型。

**注:**

*   Here, the shape of the tensor is equal to the shape of the broadcast from the end to the beginning. Where 1 is the prefix of the tensor shape as long as it has the same length as the broadcast shape.
*   In this case, input. shape [I] = shape [I], then the (i+1) th axis was consistent with the broadcast before, in this case, input.shape[i]==1 plus shape[i]==N, then the input tensor is covered by this axis *n* times.

**语法:**

```
tf.broadcastTo(x, shape)
```

**参数:**

*   **x:** is the input of the tensor, which can be of tf type. Tensor, type or array.
*   **Shape:** It is the specified shape that is input to broadcast.

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([1, 2, 3, 4]);

// Calling broadcastTo() method and
// Printing output
tf.broadcastTo(y, [1, 4]).print();
```

**输出:**

```
Tensor
     [[1, 2, 3, 4],]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling broadcastTo() method and
// Printing output
tf.broadcastTo(tf.tensor1d([3.6, 5.8, 3.7, 1.4, 9.3, 10.5]), 
                           [1, 6]).print();
```

**输出:**

```
Tensor
     [[3.5999999, 5.8000002, 3.7, 1.4, 9.3000002, 10.5],]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#broadcastTo