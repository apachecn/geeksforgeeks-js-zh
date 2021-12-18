# tensorflow . js TF . encoddestring()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-encoderstring-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-encodestring-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。encodeString()函数**用于借助给定的编码方案将所述字符串编码成字节。

**语法:**

```
tf.encodeString(s, encoding?)
```

**参数:**

*   **s:** 是要编码的指定字符串。它属于字符串类型。
*   **编码:**是要使用的编码方案。缺省值是 utf-8。

**返回值:**返回 Uint8Array。

**例 1:** 未提供编码方案时。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling tf.encodeString() method and
// printing output
console.log(tf.util.encodeString("fghi"));
```

**输出:**

```
102,103,104,105
```

**示例 2:** 当提供编码方案时。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining string and encoding
// scheme
var str = "1234"
var encoding = "utf-8"

// Calling tf.encodeString() method and
// printing output
var x = tf.util.encodeString(str, encoding);
console.log(x);
```

**输出:**

```
49,50,51,52
```

**参考:**T2】https://js.tensorflow.org/api/latest/#encodeString