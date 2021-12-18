# tensorlow . js TF . batch tospace()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-batchtospace-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.batchToSpaceND()** 函数用于将给定的“批次”从零维重构为“M+1”维，其形状为“块-形状+[批次]”，其中块-形状是参数，批次是指定的张量。这里裁剪是根据给定的裁剪数组对中间结果进行的。

```
tf.batchToSpaceND (x, blockShape, crops)
```

**参数:**该函数接受三个参数，如下图所示:

*   **x:**N 维的指定批次张量，其形状为“[批次] +空间形状+剩余形状”，其中空间形状为 M 维。
*   **块形状:**一维数组的形状必须为[M]，因为所有值都必须大于或等于 1。
*   **作物:**一种二维数组形状，其[M，2]的所有值必须大于或等于 0。这里裁剪[i] = [cropStart，cropEnd]，它定义了要从输入维度 i + 1 裁剪的部分。

**返回值:**返回指定批次的变形版本的张量。

**例 1:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a 3D Tensor of batch to reshape
const x = tf.tensor3d([5, 10, 15, 20, 25], [5, 1, 1]);

// Initializing blockShape and crops parameter
const blockShape = [1, 1];
const crops = [[0, 0], [0, 0]];

// Calling the .batchToSpaceND() function over
// the above parameters and Tensor
x.batchToSpaceND(blockShape, crops).print();
```

**输出:**

```
Tensor
    [ [[5 ],],

      [[10],],

      [[15],],

      [[20],],

      [[25],]]
```

**例 2:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a 4D Tensor of batch to restructure
const x = tf.tensor4d([0, 2, 4, 6, 8, 10], [6, 1, 1, 1]);

// Using the blockShape and crops as the parameter
// for the .batchToSpaceND() function
x.batchToSpaceND([3, 2], [[0, 0], [0, 0]]).print();
```

**输出:**

```
Tensor
    [[[[0 ],
       [2 ]],

      [[4 ],
       [6 ]],

      [[8 ],
       [10]]]]
```

**参考资料:**[https://js . tensorlow . org/API/latest/# batchtospace nd](https://js.tensorflow.org/api/latest/#batchToSpaceND)