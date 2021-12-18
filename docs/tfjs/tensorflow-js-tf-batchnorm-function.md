# tensorlow . js TF . batch norm()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-batch standard-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。batchNorm()函数**在批处理规范化中很有用。

此外，*表示*、*方差*、*标度*，包括*偏移*可以是两种形状:

*   May be the same shape as the input.
*   Generally, the depth is the last size of the input tensor, so the value can be tf. Tensor 1D of shape [depth].

**语法:**

```
tf.batchNorm(x, mean, variance, offset?, scale?, varianceEpsilon?)
```

**参数:**

*   **X:** The input tensor. It can be tf type. Tensor, type or array.
*   **means the average tensor described in** . It can be tf type. Tensor. Tensor 1, type 1 or array.
*   **Variance:** The variance tensor stated. It can be tf type. Tensor. Tensor 1, type 1 or array.
*   **Offset: the offset tensor described in** . It is optional and can be of tf type. Tensor. Tensor 1, type 1 or array.
*   **Scale: the scale tensor described in** . It is optional and can be of tf type. Tensor. Tensor 1, type 1 or array.
*   **Variable ε: the secondary floating-point number described in** in order to avoid division by 0\. It is optional and of numeric type.

**返回值:**返回 tf.Tensor

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining input tensor
const a = tf.tensor1d([1, 5, 3]);

// Defining mean
const b = tf.tensor1d([1, 1, 2]);

// Defining variance
const c = tf.tensor1d([1, 0, 1]);

// Calling batchNorm() function
tf.batchNorm(a, b, c).print();
```

**输出:**

```
Tensor
    [0, 126.4911041, 0.9995003]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining input tensor
const a = tf.tensor1d([1, 5, 3]);

// Defining mean
const b = tf.tensor1d([1, 1, 2]);

// Defining variance
const c = tf.tensor1d([1, 0, 1]);

// Defining offset
const d = tf.tensor1d([1, 6, 2]);

// Defining scale
const e = tf.tensor1d([1, 0, 1]);

// Calling batchNorm() function
a.batchNorm(b, c, d, e, 9).print();
```

**输出:**

```
Tensor
    [1, 6, 2.3162277]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#batchNorm