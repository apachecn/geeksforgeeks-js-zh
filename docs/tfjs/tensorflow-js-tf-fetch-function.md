# Tensorflow.js tf.fetch()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-fetch-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-fetch-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。fetch()功能**用于返回 *fetch* 的平台专用操作。此外，如果提取被指定为与全局对象(即窗口、进程等)相联系，那么 *tf.util.fetch* 返回该函数，否则返回平台专用的解释。

**语法:**

```
tf.fetch(path, requestInits?)
```

**参数:**

*   **路径:**是所述的字符串类型的路径。
*   **请求初始化:**所述的*请求初始化*。它是可选的，并且是字符串类型。

**返回值:**返回*回应*的承诺。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling fetch() method with respect 
// to global
const res = tf.env().global.fetch(
'https://js.tensorflow.org/api/latest/#tf.Sequential.evaluateDataset');

// Printing output
console.log(res);
```

**输出:**

```
[object Response]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling fetch() method
const res = await tf.util.fetch(
  'https://js.tensorflow.org/api/latest/#fetch');

// Printing output
console.log(JSON.stringify(res));
```

**输出:**

```
{}
```

**参考:**T2】https://js.tensorflow.org/api/latest/#fetch