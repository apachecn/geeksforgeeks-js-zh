# tensorlow . js TF . flood rdiv()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-flood rdiv-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.floorDiv()** 函数用于按元素划分两个张量，返回的结果用 floor 函数舍入。它支持广播。

**语法:**

```
tf.floorDiv (a, b)
```

**参数:**该函数接受两个参数，如下图所示:

*   **a:** 第一个输入张量作为分子。
*   **b:** 第二个输入张量为分母。它应该，必须具有与“a”相同的数据类型。

**返回值:**返回 a/b 取整结果的张量，其中 a 为第一张量，b 为第二张量。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing two Tensors
const a = tf.tensor1d([2, 5, 14, 12]);
const b = tf.tensor1d([1, 3, 4, 10]);

// Calling the .floorDiv() function over the
// above Tensors as its parameters
a.floorDiv(b).print();
```

**输出:**

```
Tensor
[2, 1, 3, 1]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Broadcasting div a with b
const a = tf.tensor1d([3, 5, 15, 17]);
const b = tf.scalar(2);

// Calling the .floorDiv() function over the
// above Tensors as its parameters
a.floorDiv(b).print();
```

**输出:**

```
Tensor
[1, 2, 7, 8]
```