# tensorflow . js TF . spectral . rfft()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-spectral-rfft-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-spectral-rfft-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**TF . spectrum . rfft()**函数用于 rfft(实值输入快速傅立叶变换)，即它在实值输入的最内部维度上计算一维离散傅立叶变换。

**语法:**

```
tf.spectral.rfft(input, fftLength)
```

**参数:**

*   **输入:**正在执行 rfft 的复杂输入。
*   **fftlelength:**为可选参数。

**返回值:**返回实际输入值最内部维度上的一维离散傅立叶变换的计算结果。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a real 1D input values
const real = tf.tensor1d([2, 4, 6]);

// Calling the .spectral.rfft() function
real.rfft().print();
```

**输出:**

```
Tensor
   [12 + 0j, -2.999999 + 1.7320514j]
```

**例二:**

## Javascript

```
// Importing the tensorflow library
import * as tf from "@tensorflow/tfjs"

// Using a real 1D input values for
// the .rfft() function
tf.tensor1d([1, 2, 3, 4]).rfft().print();
```

**输出:**

```
Tensor
   [10 + 0j, -2 + 2j, -2 + 0j]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#spectral.rfft