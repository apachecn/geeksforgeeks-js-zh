# tensorflow . js TF . decdestroing()函数

> 原文:[https://www . geeksforgeeks . org/tensorflow-js-TF-decoderstring-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-decodestring-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。decodeString()函数**用于在给定编码方案的帮助下将所述字节解码为字符串。

**语法:**

```
tf.decodeString(bytes, encoding?)
```

**参数:**

*   **字节:**是要解码的规定字节。它是 *Uint8Array* 型。
*   **编码:**是要使用的编码方案。缺省值是 utf-8。

**返回值:**返回字符串。

**示例 1:** 当提供编码方案时。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining array ArrayBuffer
var buffer = new ArrayBuffer(13);

// Defining bytes to be decoded
var y = new Uint8Array(buffer);
y[1] = 89;

// Calling tf.decodeString() method and
// printing output
const str = tf.util.decodeString(y, "ASCII");
console.log(str);
```

**输出:**

```
Y
```

**例 2:** 未提供编码方案时。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining array ArrayBuffer
var buffer = new ArrayBuffer(13);

// Defining bytes to be decoded
var y = new Uint8Array(buffer);
y[1] = 75;

// Calling tf.decodeString() method and
// printing output
console.log(tf.util.decodeString(y));
```

**输出:**

```
K
```

**参考:**T2】https://js.tensorflow.org/api/latest/#decodeString