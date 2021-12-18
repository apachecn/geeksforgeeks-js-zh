# Tensorflow.js tf。张量类。处置()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-tensor-class-dispose-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-class-dispose-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。处置()功能**用于处置所述 *tf。张量*来自记忆。

**语法:**

```
dispose()
```

**参数:**此方法不保存任何参数。

**返回值:**返回 void。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a tensor
const t = tf.tensor([6, 7]);

// Calling dispose() method
t.dispose();

// Printing output
console.log("Tensor Disposed.")
```

**输出:**

```
Tensor Disposed.
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a 2d tensor
const tn = tf.tensor2d([6, 7], [1, 2]);

// Calling dispose() method
const y = tn.dispose();

// Printing output
console.log(tn)
```

**输出:**

```
An error occured on line: 11
Tensor is disposed.
```

这里，打印张量输出时发生错误，因为张量已经被处理掉了。

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.Tensor.dispose