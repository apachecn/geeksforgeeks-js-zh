# 张量流.js tf.concat（） 函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-concat-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.concat()** 函数用于沿着给定的轴连接指定张量的列表。

**语法:**

```
tf.concat (tensors, axis)
```

**参数:**该函数接受两个参数，如下图所示:

*   **张量:**它是要连接的指定张量的列表。
*   **轴:**是执行连接过程的轴。它是一个可选参数，默认值为 0。

**返回值:**它返回串联张量的张量。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing two tensors to cancatenate
const A = tf.tensor1d([0, 2, 4]);
const B = tf.tensor1d([1, 3, 5]);

// Calling the .concat() function over
// the above tensors as its parameters
A.concat(B).print();
```

**输出:**

```
Tensor
   [0, 2, 4, 1, 3, 5]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing three 2-D tensors to cancatenate
const A = tf.tensor2d([[0, 2], [1, 3]]);
const B = tf.tensor2d([[4, 6], [5, 7]]);
const C = tf.tensor2d([[8, 10], [9, 11]]);

// Initializing axis parameter
const axis = 1;

// Calling the .concat() function over
// the above tensors and axis as its parameters
tf.concat([A, B, C], axis).print();
```

**输出:**

```
Tensor
   [[0, 2, 4, 6, 8, 10],
    [1, 3, 5, 7, 9, 11]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#concat