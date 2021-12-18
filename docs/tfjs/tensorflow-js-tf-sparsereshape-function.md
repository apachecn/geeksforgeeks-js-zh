# tensorflow . js TF . sparsereshape()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sparsereshape-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-sparsereshape-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。**。sparseReshape()函数**在渲染的压缩张量上拥有相同的语法，如*重塑()*函数。其中输入指数根据所需的新形状重新计算。

**注意:**

*   In this case, one element of the new shape is a different value, that is, -1, then the size of this dimension is calculated so that the count of dense size remains unchanged.
*   At most, only one component of the new shape is -1.
*   Here, the count of compressed components indicated by the new shape should be the same as the count of compressed components initially indicated by the input shape.
*   *shaping* cannot affect the order of the values in the sparse tensor.
*   If the input tensor has rank *r _ in* and n loading values, and the new shape has length *r _ out* , then the shape of the input index is *n* , *r _ in* ], and the length of the input shape is *r _ in [*

**语法:**

```
tf.sparseReshape(inputIndices, inputShape, newShape)
```

**参数:**该方法接受以下参数:

*   **输入项:**是所述的二维 N×R _ in 矩阵以及稀疏张量中加载值的索引。它可以是 tf 类型。张量 2D、TypedArray 或数组。
*   **输入形状:**它是所述的 1-D. R_in 张量 1D 以及输入稀疏张量的压缩形状。它可以是 tf 类型。张量 1、类型 1 或数组。
*   **新形状:**这是所述的 1 维 R_out 张量 1 以及所需的新压缩形状。它可以是 tf 类型。张量 1、类型 1 或数组。

**返回值:**返回 *tf。张量*对象。

**示例 1:** 在下面的示例中，我们调用了 sparse.sparseReshape()函数及其所有参数，并打印了没有其索引和形状的输出响应。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs")

// Calling sparse.sparseReshape() function
// with all its parameter
const res = tf.sparse.sparseReshape(
    [[1, 0, 1], [2, 0, 1], [1, 1, 2], [0, -1, 0], [-3, 1, 2]],
    [1, 2, 9], [-1, 9]);

// Printing output
console.log(res);
```

**输出:**

```
{
  "outputIndices": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [
      5,
      2
    ],
    "dtype": "float32",
    "size": 10,
    "strides": [
      2
    ],
    "dataId": {
      "id": 82
    },
    "id": 82,
    "rankType": "2",
    "scopeId": 36
  },
  "outputShape": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [
      2
    ],
    "dtype": "float32",
    "size": 2,
    "strides": [],
    "dataId": {
      "id": 83
    },
    "id": 83,
    "rankType": "1",
    "scopeId": 36
  }
}
```

**示例 2:** 在下面的示例中，我们调用了 sparse.sparseReshape()函数及其所有参数，并打印了输出响应及其索引和形状。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs")

// Calling sparse.sparseReshape() function
// with all its parameter
const res = tf.sparse.sparseReshape(
    [[1.1, 0, 1.2], [2.1, 0.2, 1.3], [1.4, 2.3, 2.5], [null, -1, 0], [-3, 1, 2]],
    [1.0, 3, 3], [-1, 9]);

// Printing output indices
res['outputIndices'].print();

// Printing output shape
res['outputShape'].print();
```

**输出:**

```
Tensor
    [[1 , 2 ],
     [2 , 2 ],
     [2 , 3 ],
     [0 , -3],
     [-2, -4]]
Tensor
    [1, 9]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#sparseReshape