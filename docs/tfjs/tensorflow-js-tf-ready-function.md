# Tensorflow.js tf.ready()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-ready-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-ready-function/)

**简介:** Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型以及深度学习神经网络。

**。ready()函数**用于返回一个承诺，该承诺确定最近选择的后端或最高优先级的后端在什么时候被初始化。此外，如果我们使用拥有异步初始化的后端，我们需要等待这个承诺。

**语法:**

```
tf.ready()
```

**参数:**此方法不保存任何参数。

**返回值:**返回无效承诺。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling setBackend() method
tf.setBackend('wasm');

// Calling ready() method and
// Printing output
await tf.ready().then(() => {
  console.log(tf.backend().blockSize)
});
```

**输出:**

```
48
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling setBackend() method
tf.setBackend('webgl');

// Calling ready() method and
// Printing output
await tf.ready().then(() => {
  console.log(JSON.stringify(tf.getBackend()))
});
```

**输出:**

```
"webgl"
```

**参考:**T2】https://js.tensorflow.org/api/latest/#ready