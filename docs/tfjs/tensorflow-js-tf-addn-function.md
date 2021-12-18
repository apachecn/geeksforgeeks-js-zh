# tensorlow . js TF . add n()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-addn-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.addN()** 函数用于逐元素添加指定的张量列表。每个张量应该具有相同的形状和数据类型。

**语法:**

```
tf.addN (tensors)
```

**参数:**该函数接受如下所示的参数:

*   **张量:**具有相同形状和数据类型的指定张量的数组/列表。

**返回值:**返回一个添加元素的张量。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing some Tensors
const a = tf.tensor1d([0, 1, 2]);
const b = tf.tensor1d([3, 4, 5]);

// Calling the .addN() function over
// the above Tensors as its parameters
tf.addN([a, b]).print();
```

**输出:**

```
Tensor
   [3, 5, 7]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using some Tensors as the parameter
// for the .addN() function 
tf.addN([[12, 5, 6], [3, 2, 5], [2, 7, 9]]).print();
```

**输出:**

```
Tensor
   [17, 14, 20]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#addN