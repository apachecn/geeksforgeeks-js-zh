# Tensorflow.js tf.signal.stft()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-signal-STFT-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-signal-stft-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

函数用于计算信号的短时傅里叶变换。

**语法** :

```
tf.signal.stft (signal, frameLength, frameStep, 
                     fftLength?, windowFn?) 
```

**参数**:

*   **信号:**一维实值张量。
*   **帧长:**样本的窗口长度。
*   **帧步长:**要步进的样本数。
*   **FFT 长度:**FFT 的大小。
*   **windowFn:** 一个取窗长的可调用。

**返回值:**返回 tf.Tensor

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

const input = tf.tensor1d([3, 4, 6])
tf.signal.stft(input, 3, 1).print();
```

**输出:**

```
Tensor
     [[4 + 0j, 0 + -4j, -4 + 0j],]

```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

const input = tf.tensor1d([1, 2, 3, 4, 5, 6, 7])
tf.signal.stft(input, 3, 1).print();
```

**输出:**

```
Tensor
    [[2 + 0j, 0 + -2j, -2 + 0j],
     [3 + 0j, 0 + -3j, -3 + 0j],
     [4 + 0j, 0 + -4j, -4 + 0j],
     [5 + 0j, 0 + -5j, -5 + 0j],
     [6 + 0j, 0 + -6j, -6 + 0j]]
```

**参考:**[**https://js.tensorflow.org/api/latest/#signal.stft**](https://js.tensorflow.org/api/latest/#signal.stft)