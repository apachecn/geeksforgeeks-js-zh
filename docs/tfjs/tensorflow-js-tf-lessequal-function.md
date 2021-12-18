# tensorlow . js TF . lesequal()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-lesequal-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**TF . leseqal()**函数用于返回两个指定张量值的布尔值张量，即如果第一个张量值小于或等于第二个张量值，则返回真，否则返回假。它支持广播。

**语法:**

```
tf.lessEqual(a, b)
```

**参数:**该函数接受两个参数，如下图所示:

*   **a:** 第一个输入张量。
*   **b:** 第二个输入张量。它应该具有与张量“a”相同数据类型的值。

**返回值:**它返回布尔值的张量，即如果第一个张量的值小于或等于第二个张量的值，则返回 true，否则返回 false。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing two different tensors
const a = tf.tensor1d([1, 3, 6, 7]);
const b = tf.tensor1d([1, 4, 5, 9]);

// Calling the .lessEqual() function
a.lessEqual(b).print();
```

**输出:**

```
Tensor
   [true, true, false, true]
```

**例二:**

## Javascript

```
// Importing the tensorflow library
import * as tf from "@tensorflow/tfjs"

// Calling the .lessEqual() function with two
// Different tensors as its parameters
tf.tensor1d([1.5, 2.060, 2, 0.05, 4.5]).
lessEqual(tf.tensor1d([1.25, 2.60, 2.0, .5, 4.05])).print();
```

**输出:**

```
Tensor
   [false, true, true, true, false]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#lessEqual