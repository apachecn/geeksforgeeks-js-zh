# Tensorflow.js tf.linalg.qr（） 函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-linalg-QR-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**.linalg.qr()函数**用于应用户主变换，通过 n 矩阵计算参考 m 的 qr 分解。

**语法:**

```
tf.linalg.qr(x, fullMatrices?)
```

**参数:**

*   **x:** 规定的 tf。待二维码分解的张量。它的等级必须大于或等于 2。假设，它的形状为[…，M，N]。它是 tf.Tensor 类型的。
*   **full Matrix:**它是一个可选参数，属于布尔值类型，默认值为 false。如果是真的，那么它评估正常大小的 *Q* 否则它评估的只是最高的 *N* 列 *Q* 和 *R* 。

**返回值:**返回【tf。张量。张量】。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining a 2d tensor
const tn = tf.tensor2d([[3, 5], [7, 2]]);

// Calling linalg.qr() function
let [Q, R] = tf.linalg.qr(tn);

// Printing outputs
console.log('q');
Q.print();
console.log('r');
R.print();
```

**输出:**

```
q
Tensor
    [[-0.3939192, 0.919145  ],
     [-0.919145 , -0.3939193]]
r
Tensor
    [[-7.6157722, -3.8078861],
     [0         , 3.8078861 ]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining a 2d tensor
const tn = tf.tensor2d([[3, 5], [7, 2]]);

// Calling linalg.qr() function
let [Q, R] = tf.linalg.qr(tn, true);

// Printing outputs
console.log('Orthogonalized:');
Q.transpose().print();
console.log('Regenerated:');
R.dot(Q).print();
```

**输出:**

```
Orthogonalized:
Tensor
    [[-0.3939192, -0.919145 ],
     [0.919145  , -0.3939193]]
Regenerated:
Tensor
    [[6.4999986 , -5.499999 ],
     [-3.4999995, -1.4999998]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#linalg.qr