# Tensorflow.js tf.engine()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-engine-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-engine-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。engine()函数**用于返回全局引擎，该引擎保存每个张量的路径以及后端。

**语法:**

```
tf.engine()
```

**参数:**此方法不保存任何参数。

**返回值:**返回引擎。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling engine() and startScope()
// method
tf.engine().startScope();  

// Calling ones() method
const res = tf.ones([200, 250]);

// Printing output
console.log(res);
```

**输出:**这里，范围没有结束，所以返回一个张量。

```
Tensor
    [[1, 1, 1, ..., 1, 1, 1],
     [1, 1, 1, ..., 1, 1, 1],
     [1, 1, 1, ..., 1, 1, 1],
     ...,
     [1, 1, 1, ..., 1, 1, 1],
     [1, 1, 1, ..., 1, 1, 1],
     [1, 1, 1, ..., 1, 1, 1]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling engine() and startScope()
// method
tf.engine().startScope();  

// Calling ones() method
const t1 = tf.ones([200, 250]);

// Calling tidy() and min() method
// with respect to t1
const t2 = tf.tidy(() => t1.min());

// Calling engine() and endScope()
// method
tf.engine().endScope();

// Printing output
console.log(t2);
```

**输出:**这里，范围结束，因此合成张量被处理。

```
An error occured on line: 20
Tensor is disposed.
```

**参考:**T2】https://js.tensorflow.org/api/latest/#engine