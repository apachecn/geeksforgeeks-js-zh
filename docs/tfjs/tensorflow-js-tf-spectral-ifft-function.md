# tensorflow . js TF . spectrum . IFFT()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-spectral-IFFT-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-spectral-ifft-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**TF . spectrum . ifft()**函数用于 IFFT(快速傅里叶逆变换)，即它在输入的最内部维度上计算一维离散傅里叶逆变换。

**语法:**

```
tf.spectral.ifft(input)
```

**参数:**

*   **输入:**正在执行 ifft 的复数输入。

**返回值:**返回输入最内部维度的一维离散傅里叶逆变换的计算结果。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a real and imaginary 1D input values
const real = tf.tensor1d([1, 5]);
const imag = tf.tensor1d([2, 4]);
const x = tf.complex(real, imag);

// Calling the .spectral.ifft() function
// over the input parameter value x
tf.spectral.ifft(x).print();
```

**输出:**

```
Tensor
   [3 + 3j, -2 + -1j]
```

**例二:**

## Javascript

```
// Importing the tensorflow library
import * as tf from "@tensorflow/tfjs"

// Using a real and imaginary 1D input values as the
// parameter for the .complex() function
const x = tf.complex(tf.tensor1d([5, 10, 15, 20]), tf.tensor1d([1, 2, 3, 4]));

// Calling the .spectral.ifft() function
// over the input parameter value x
tf.spectral.ifft(x).print();
```

**输出:**

```
Tensor
   [12.5 + 2.5j, -2 + -3j, -2.5 + -0.5j, -3 + 2j]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#spectral.ifft