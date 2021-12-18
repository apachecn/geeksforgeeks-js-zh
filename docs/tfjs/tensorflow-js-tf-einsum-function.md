# tensorlow . js TF . un um()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-un um-function/

**Tensorflow.js** 是谷歌正在开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

那个。 **einsum()函数**用于指定指数和外积上的张量收缩。

**语法:**

```
tf.einsum (equation, tensors)
```

**参数:**

*   **方程:**它是第一个输入张量元素，是描述收缩的字符串，格式与 numpy.einsum 相同。
*   **。。。张量:**它是第二个输入张量元素，其中输入用于收缩(每个张量一个张量)，其形状应与方程一致。

**限制:**

*   2 input tensors are not supported.
*   It does not support any repetitive axis of the given input tensor. For example, the formula "ii→" is not supported.
*   The … symbol is not supported.

**返回值:**返回<u>**<u>TF . tensor .</u>**</u>

<u>**例 1:** 在这个例子中，我们讲的是像矩阵乘法这样的特例。</u>

## <u>Javascript</u>

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining the first tensor input elements
const a = tf.tensor2d([[1, 1, 3], [4, 3, 6]]);

// Defining the second input tensor elements
const b = tf.tensor2d([[1, 1], [2, 3], [4, 5]]);

// Calling the einsum() function and printing outputs 
tf.einsum('ij,jk->ik', a, b).print();
```

<u>**输出:**</u>

```
Tensor
    [[14, 19],
     [30, 43]]
```

<u>**例 2:** 在这个例子中，我们讲的是像点积这样的特例。</u>

## <u>Javascript</u>

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining the first input elements
const x = tf.tensor1d([1, 1, 3]);

// Defining the second input elements
const y = tf.tensor1d([1, 1, 2]);

// Calling the einsum() function
// and printing outputs 
tf.einsum('i,i->', x, y).print();
```