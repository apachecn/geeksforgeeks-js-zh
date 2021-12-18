# tensorlow . js TF . space tobachtnd()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-space tobaccond-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.spaceToBatchND()** 函数用于将指定输入空间的空间维度拆分为块形状为 blockShape 的块矩阵，其中 blockshape 为参数。这里的空间维度是根据指定的填充数组填充的。

**语法:**

```
tf.spaceToBatchND (x, blockShape, paddings)
```

**参数:**该函数接受三个参数，如下图所示:

*   **x:** 形状为“[批处理] +空间形状+剩余形状”的 N 维指定张量，其中空间形状具有 M 维。
*   **块形状:**必须是形状为[M]的一维数组，因为所有值都必须大于或等于 1。
*   **填充:**形状为[M，2]的二维数组，所有值必须大于或等于 0。这里填充等于[padStart，padEnd]。

**返回值:**返回指定输入空间的分裂版本的张量。

**例 1:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a Tensor
const x = tf.tensor4d(
    [5, 10, 15, 20, 25, 30],
    [1, 3, 2, 1]
);

// Initializing blockShape and paddings parameters
const blockShape = [1, 1];
const paddings = [[0, 0], [0, 0]];

// Calling the .spaceToBatchND() function over
// the above parameters and Tensor
x.spaceToBatchND(blockShape, paddings).print();
```

**输出:**

```
Tensor
   [[[[5 ],
      [10]],

     [[15],
      [20]],

     [[25],
      [30]]]]
```

**例 2:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a Tensor
const x = tf.tensor4d([2, 4, 6, 8], [1, 2, 2, 1]);

// Using the blockShape and paddings as the
// parameter for the .spaceToBatchND() function
x.spaceToBatchND([2, 2], [[0, 0], [0, 0]]).print();
```

**输出:**

```
Tensor
   [ [ [[2],]],

     [ [[4],]],

     [ [[6],]],

     [ [[8],]]]
```

**参考:**T2https://js.tensorflow.org/api/latest/#spaceToBatchND