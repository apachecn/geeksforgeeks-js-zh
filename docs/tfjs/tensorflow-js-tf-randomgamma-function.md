# tensorlow . js TF . ranmgamma()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-ranmgamma-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.randomGamma()** 函数用于创建 tf。从伽玛分布中取样的张量。

**语法:**

```
tf.randomGamma(shape, alpha, beta, dtype, seed)
```

**参数:**该函数接受三个参数，如下图所示:

*   **形状:**定义输出张量形状的整数数组。
*   **α**:伽玛分布的形状参数。
*   **beta** :可选参数。伽玛分布的逆标度参数。默认值为 1。
*   **数据类型:**输出的数据类型。可能的数据类型值是“float32”或“int32”。这也是一个可选的参数。
*   **seed:** 是可选参数。随机数生成器的种子。

**返回:**返回 tf。张量

**例 1:**

## Javascript

```
// Importting the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor with values sampled 
// from a gamma distribution
const x=tf.randomGamma([5], 0);

// Printing the tensor
x.print();
```

**输出:**

```
Tensor
    [0, 0, 0, 0, 0]
```

**例二:**

## Javascript

```
// Importting the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor with values sampled 
// from a gamma distribution
const x=tf.randomGamma([5], 1);

// Printing the tensor
x.print();
```

**输出:**

```
Tensor
    [1.4808178, 1.6668015, 0.9527208, 1.6024575, 1.6021353]
```

**例三:**

## Javascript

```
// Importting the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor with values sampled
// from a gamma distribution
const x=tf.randomGamma([2,2], 1);

// Printing the tensor
x.print();
```

**输出:**

```
Tensor
    [[0.1157758, 1.4427431],
     [0.4978852, 0.1617882]]
```

**例 4:**

## Javascript

```
// Importting the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor with values sampled 
// from a gamma distribution
const x=tf.randomGamma([5], 1,2,'int32',98);

// Printing the tensor
x.print();
```

**输出:**

```
Tensor
    [0, 1, 4, 0, 1]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#randomGamma