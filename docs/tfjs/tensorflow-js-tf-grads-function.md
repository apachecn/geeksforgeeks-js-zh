# Tensorflow.js tf.grads()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-grads-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-grads-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**函数取函数 f(x)并返回函数 gx**

**语法** :

```
tf.grads (f)
```

**参数**:

*   **f:** 这是计算梯度的给定函数。

**返回值**:返回数组。

**例 1:**

## Javascript

```
// Importing the @tensorflow/tjs library
const tf=require("@tensorflow/tfjs")
const f = (a, b) => b.add(a);

// Grad function is used
const g = tf.grads(f);

// Tensor is declared
const a = tf.tensor1d([5, 6]);
const b = tf.tensor1d([-10, -20]);

// Variables are defined
const [gfg1] = g([b, a]);

// Variable is printed
gfg1.print();
```

**输出:**

```
Tensor
    [1, 1]
```

**例二:**

## Javascript

```
// Importing the @tensorflow/tfjs library
const tf=require("@tensorflow/tfjs")
const f = (a) => a.mul(8);

// Grad function is used
const g = tf.grads(f);

// Tensor is declared
const a = tf.tensor1d([50, 60]);

// Variables are defined
const [gfg1] = g([a]);

// Variable is printed
gfg1.print();
```

**输出:**

```
Tensor
    [8, 8]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#grads