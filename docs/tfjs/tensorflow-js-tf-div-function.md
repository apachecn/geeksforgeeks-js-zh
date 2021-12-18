# tensorlow . js TF . div()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-div-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.div()** 函数用于按元素划分两个指定的张量。它支持广播。

**语法:**

```
tf.div (a, b)
```

**参数:**该函数接受两个参数，如下图所示:

*   **a:** 第一个输入张量作为分子。
*   **b:** 第二个输入张量为分母。它必须具有与“a”相同的数据类型。

**返回值:**它为 a/b 的结果返回一个张量，其中 a 是第一个张量，b 是第二个张量。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing two Tensors
const a = tf.tensor1d([3, 5, 10, 15]);
const b = tf.tensor1d([2, 5, 2, 7]);

// Calling the .div() function over the 
// above Tensors as its parameters
a.div(b).print();
```

**输出:**

```
Tensor
   [1.5, 1, 5, 2.1428571]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Broadcasting the div a with b
const a = tf.tensor1d([1, 12, 17, 20]);
const b = tf.scalar(3);

// Calling the .div() function over the 
// above Tensors as its parameters
a.div(b).print();
```

**输出:**

```
Tensor
   [0.3333333, 3.9999998, 5.6666665, 6.666666]
```