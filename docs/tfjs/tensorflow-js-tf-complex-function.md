# Tensorflow.js tf.complex()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-complex-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-complex-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。帮助开发者在 JavaScript 中开发 ML 模型，直接在浏览器或者 Node.js 中使用 ML。

**tf.complex()函数**用于将两个实数转换为复数。

**语法:**

```
tf.complex(real, imag)
```

**参数:**

*   **real:** 可以是这三个 tf 中的任意一个。张量、类型或数组。它代表形成的复数的实部。
*   **imag:** 也可以是这三个 tf 中的任意一个。张量、类型或数组。它代表形成的复数的虚部。

**返回值:**返回一个 tf.Tensor

**注:**实参数为 tf。张量代表复数的实部，imag 参数是 tf。张量表示复数的虚部。
例如，

*   设实数为[r0，r1，r2]
*   设 imag 为[i0，i1，i2]
*   转换后的复数将是[r0 + i0，r1 + i1，r2 + i2]

**例 1:**

## java 描述语言

```
// The complex function containing the
// real and imag Typedarray
const complex = tf.complex ([5,3],[1,3]);

// Printing the tensor
complex.print();
```

**输出:**

```
Tensor
   [5 + 1j, 3 + 3j]
```

**例 2:**

## java 描述语言

```
// The complex function containing the
// real and imag Typedarray
const complex = tf.complex(
    tf.tensor1d([4.75, 5.75]),
    tf.tensor1d([2.25, 3.25])
);

// Printing the tensor
complex.print();
```

**输出:**

```
Tensor
   [4.75 + 2.25j, 5.75 + 3.25j]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#complex