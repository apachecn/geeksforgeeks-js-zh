# tensorlow . js TF . argmin()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-argmin-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.argMin()** 函数用于返回指定张量沿轴的最小值的索引。输出结果具有与输入相同的形状，沿轴的尺寸被移除。

**语法:**

```
tf.argMin (x, axis)
```

**参数:**该函数接受两个参数，如下图所示:

*   **x:** 输入张量。
*   **轴:**要减少的指定尺寸。它是一个可选参数，默认值为 0。

**返回值:**它返回沿轴的最小值的指数张量。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a some tensors 
const a = tf.tensor1d([0, 1]);
const b = tf.tensor1d([5, 3]);
const c = tf.tensor1d([6, 3, 5, 2]);

// Calling the .argMin() function over 
// the above tensors
a.argMin().print();
b.argMin().print();
c.argMin().print();
```

**输出:**

```
Tensor
   0
Tensor
   1
Tensor
   3
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a some tensors 
const a = tf.tensor1d([0, 1]);
const b = tf.tensor2d([9, 5, 2, 8], [2, 2]);
const c = tf.tensor1d([6, 4, 7]);

// Initializing a axis parameters
const axis1 = -1;
const axis2 = -2;
const axis3 = 0;

// Calling the .argMin() function over 
// the above tensors
a.argMin(axis1).print();
b.argMin(axis2).print();
c.argMin(axis3).print();
```

**输出:**

```
Tensor
   0
Tensor
   [1, 0]
Tensor
   1
```

**参考:**T2】https://js.tensorflow.org/api/latest/#argMin