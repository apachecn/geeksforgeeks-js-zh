# tensorlow . js TF .稀疏()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-稀疏函数/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**函数用于将指定的稀疏表示转换为稠密张量。如果给定的索引重复出现，最终值将与该索引的所有值相加。**

**语法:**

```
tf.sparseToDense(sparseIndices, sparseValues, 
            outputShape, defaultValue)
```

**参数:**该函数接受四个参数，如下图所示:

*   **稀疏张量:**它是 int32 数据类型的 0 维、1 维或 2 维张量。在这里，稀疏赋值[i]放在稀疏索引[i]处，其中 I 是索引值。
*   **稀疏赋值:**它是一个 0 维或 1 维的值张量，对应于每一行稀疏赋值。
*   **outputShape:** 是转换后的稠密输出张量的形状。
*   **默认值:**是为稀疏字典中未指定的索引设置的值。它的默认值为零。这是一个可选参数。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing indices and values
const indices = tf.tensor1d([4, 3, 2, 1, 0], 'int32');
const values = tf.tensor1d([1111, 111, 11, 1, 0.1], 'float32');

// Specifying shape for the output dense
const shape = [7];

// Getting the Dense representation for the above
// sparse representation
tf.sparseToDense(indices, values, shape).print();
```

**输出:**

```
 Tensor
   [0.1, 1, 11, 111, 1111, 0, 0]
```

**例 2:**

## 【JavaScript】

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing indices and values
const indices = tf.tensor1d([1, 2, 3], 'int32');
const values = tf.tensor1d([10, 20, 30], 'float32');

// Getting the Dense representation for the above
// sparse representation along with shape of [6]
// and default value of 55
tf.sparseToDense(indices, values, [6], 55).print();
```

**输出:**

```
Tensor
   [55, 10, 20, 30, 55, 55]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#sparseToDense