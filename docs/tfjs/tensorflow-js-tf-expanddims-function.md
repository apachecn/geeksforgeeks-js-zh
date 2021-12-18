# tensorlow . js TF . expanddims()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-expanddims-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。expandDims()** **功能**用于查找 tf。通过在张量中插入一个维度，借助张量的形状来扩展其秩的张量对象。

**语法:**

```
tf.expandDims(x, axis?)
```

**参数:**

*   **x:** 是所述的张量输入，其大小要扩展，可以是 tf 类型。张量、类型或数组。
*   **轴:**是所述的尺寸指数，1 的形状将插入该指数。缺省值为零，即第一个维度，并且是数字类型。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input and axis
const y = tf.tensor1d([5, 6, 7, 8]);
const axs = 1;

// Calling tf.expandDims() method and
// Printing output
y.expandDims(axs).print();
```

**输出:**

```
Tensor
    [[5],
     [6],
     [7],
     [8]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling tf.expandDims() method and
// Printing output
tf.expandDims(tf.tensor1d([1.2, 3.5, 7.6, 9.7]), 1).print();
```

**输出:**

```
Tensor
    [[1.2      ],
     [3.5      ],
     [7.5999999],
     [9.6999998]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#expandDims