# tensorlow . js TF . divnon()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-divnon-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.divNoNan()** 函数用于按元素划分两个张量，如果分母为 0，则返回 0。它支持广播。

**语法:**

```
tf.divNoNan (a, b)
```

**参数:**该函数接受两个参数，如下图所示:

*   **a:** 第一个输入张量作为分子。
*   **b:** 第二个输入张量为分母。它应该具有与“a”相同的数据类型。

**返回值:**它为 a/b 的结果返回一个张量，其中 a 是第一个张量，b 是第二个张量。如果分母为 0，则返回 0。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing some Tensors
const a = tf.tensor1d([2, 5, 7, 10]);
const b = tf.tensor1d([1, 3, 2, 6]);
const c = tf.tensor1d([0, 0, 0, 0]);

// Calling the .divNoNan() function
// over the above Tensors as its parameters
a.divNoNan(b).print(); 
a.divNoNan(c).print();
```

**输出:**

```
Tensor
   [2, 1.6666665, 3.5, 1.6666665]
Tensor
   [0, 0, 0, 0]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Broadcasting div a with b and c
const a = tf.tensor1d([3, 6, 11, 17]);
const b = tf.scalar(2);
const c = tf.scalar(0);

// Calling the .divNoNan() function
// over the above Tensors as its parameters
a.divNoNan(b).print(); 
a.divNoNan(c).print();
```

**输出:**

```
Tensor
   [1.5, 3, 5.5, 8.5]
Tensor
   [0, 0, 0, 0]
```