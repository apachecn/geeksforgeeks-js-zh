# tensorflow . js TF . spectrum . irfft()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-spectral-irfft-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-spectral-irfft-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**TF . spectrum . irfft()**函数用于 IRFFT(逆实值输入快速傅里叶变换)，即它计算实输入值最内部维度上的一维 IDFT(逆离散傅里叶变换)。

**语法:**

```
tf.spectral.irfft(input)
```

**参数:**

*   **输入:**正在执行*快速傅立叶变换*的复杂输入。

**返回值:**返回实际输入值最内部维度上的一维 IDFT(逆离散傅里叶变换)的计算结果。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a real and imaginary 1D input values
const real = tf.tensor1d([1, 5]);
const imag = tf.tensor1d([2, 4]);
const x = tf.complex(real, imag);

// Calling the .spectral.irfft() function
// over the parameter input real value x
tf.spectral.irfft(x).print();
```

**输出:**

```
Tensor
    [[3, -2],]
```

**例二:**

## Javascript

```
// Importing the tensorflow library
import * as tf from "@tensorflow/tfjs"

// Using a real and imaginary 1D input values as the
// parameter for the .complex() function
const x = tf.complex(tf.tensor1d([1, 2, 3, 4]), 
                     tf.tensor1d([2, 4, 6, 8]));

// Calling the .spectral.irfft() function
// over the input parameter value x
tf.spectral.irfft(x).print();
```

**输出:**

```
Tensor
    [[2.5, -3.5534179, 0.5773503, -0.1666667, -0.5773499, 2.2200849],]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#spectral.irfft