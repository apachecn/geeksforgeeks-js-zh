# tensorlow . js TF . prelu()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-prelu-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。prelu()函数**用于查找所述张量输入的泄漏整流线性以及参数α，并且是按元素进行的。

**语法:**

```
tf.prelu(x, alpha)
```

其中，x < 0？α* x:f(x)= x

**参数:**

*   **X:** is a statement tensor input, which can be of tf type. Tensor, type or array.
*   [T0】 α: 【T1] It is a specified scale factor with a specified negative value in tensor input, which can be of tf type. Tensor, type or array.

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([-11, 12, -31, 36]);

// Defining alpha
const alp = tf.scalar(0.2);

// Calling prelu() method and
// Printing output
y.prelu(alp).print();
```

**输出:**

```
Tensor
    [-2.2, 12, -6.2000003, 36]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling prelu() method and
// Printing output
var res = tf.prelu(tf.tensor1d(
  [-1.9, 8.2, -6.1, 13.6]), tf.scalar(-1));
res.print();
```

**输出:**

```
Tensor
    [1.9, 8.1999998, 6.0999999, 13.6000004]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#prelu