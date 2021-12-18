# Tensorflow.js tf.env()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-env-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-env-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。env()函数**用于返回当前环境，即一个全局实体。此外，环境对象包括评估的属性值以及动态平台。

**语法:**

```
tf.env() 
```

**参数:**该方法不保存任何参数。

**返回值:**返回 tf.Environment。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling env() and getBool() method
// along with its parameter
const res = tf.env().getBool('WEBGL_RENDER_FLOAT32_ENABLED');

// Printing output
console.log(res);
```

**输出:**

```
true
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling env() method's feature
const res1 = tf.env().features;

// Printing output
console.log(res1);
```

**输出:**

```
{
  "WEBGL_FORCE_F16_TEXTURES": false,
  "WEBGL_VERSION": 2,
  "WEBGL_RENDER_FLOAT32_CAPABLE": true,
  "WEBGL_RENDER_FLOAT32_ENABLED": true,
  "PROD": true,
  "DEBUG": true
}
```

**参考:**T2】https://js.tensorflow.org/api/latest/#env