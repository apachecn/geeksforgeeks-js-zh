# Tensorflow.js tf.keep()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-keep-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-keep-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。keep()函数**用于保持 tf.tidy()方法中形成的张量输入不被自发丢弃。

**语法:**

```
tf.keep(result)
```

**参数:**

*   **结果:**是所述张量输入被阻止被丢弃。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Declaring a variable
let res1;

// Calling tidy method
const res2 = tf.tidy(() => {

  // Defining result parameter
  const result = tf.scalar(121);

  // Calling tf.keep() method
  res1 = tf.keep(result.sqrt());
});

// Printing output
res1.print();
```

**输出:**

```
Tensor
    11
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Declaring a variable
let res1;

// Calling tidy method
const res2 = tf.tidy(() => {

  // Calling tf.keep() method with its
  // parameter
  res1 = tf.keep(tf.tensor1d(
    [1.3, 0.5, 0, NaN, null, -.5]).cos());
});

// Printing output
res1.print();
```

**输出:**

```
Tensor
    [0.2675007, 0.8775977, 1, NaN, 1, 0.8775977]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#keep