# tensorflow . js TF . drop()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-drop-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-dropout-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**TF . drop()**函数用于计算 drop。你可以从[https://www.geeksforgeeks.org/dropout-in-neural-networks/](https://www.geeksforgeeks.org/dropout-in-neural-networks/)了解更多关于辍学的信息。

**语法:**

```
tf.dropout (x, rate, noiseShape?, seed?)
```

**参数:**

*   **x:** 具有浮动输入值的张量。
*   **率(数):**x 的每个元素被丢弃的概率。接受 0 到 1 范围内的值。
*   **噪声形状(数字[]):** 表示随机生成的保留/丢弃标志的形状的数组。证明这个参数是可选的。类型:int32。
*   **种子(数字或字符串):**用于创建随机种子。提供此参数是可选的。

**返回值:**返回 tf。张量[]。

**例 1:**

## java 描述语言

```
const tf = require("@tensorflow/tfjs")

// creating a tensor
const x = tf.tensor1d([1, 2, 2, 1]);
const rate = 0.6;

// calculating dropout
const output = tf.dropout(x, rate);
output.print();
```

**输出:**

```
Tensor
   [0, 5, 5, 0]
```

**例 2:**

在这个例子中，我们将传递噪声形状为[4，1]来创建一个新的尺寸。

## java 描述语言

```
const tf = require("@tensorflow/tfjs")

// creating a tensor
const x = tf.tensor1d([1, 2, 3, 1]);
const rate = 0.6;

// calculating dropout
const output = tf.dropout(x, rate, [4,1]);
output.print();
```

**输出:**

```
Tensor
  [[0  , 0, 0  , 0  ],
   [0  , 0, 0  , 0  ],
   [2.5, 5, 7.5, 2.5],
   [2.5, 5, 7.5, 2.5]]
```

**参考:**T2https://js.tensorflow.org/api/latest/#dropout