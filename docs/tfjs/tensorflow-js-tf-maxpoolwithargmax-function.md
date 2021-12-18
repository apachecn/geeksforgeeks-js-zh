# tensorlow . js TF . maxpoolwithargmax()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-maxpoolwithargmax-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。函数**用于确定图像的 2D 最大池以及最大列表，即索引。其中，argmax 中的索引被拉平，以便位置[b，y，x，c]处的峰值变成压缩索引:(y *宽度+ x) *通道+ c 在这种情况下，include_batch_in_index 为假，如果 include_batch_in_index 为真，则它的值为((b *高度+ y) *宽度+ x) *通道+c。此外，在拉平之前，返回的索引始终在[0，高度]x[0，宽度]中。

**语法:**

```
tf.maxPoolWithArgmax(x, filterSize, 
    strides, pad, includeBatchInIndex?)
```

**参数:**

*   **x:** 所述的输入张量，其或者是等级 4 或者等级 3，并且具有形状:【批次、高度、宽度、英寸通道】。此外，在等级为 3 的情况下，则假定批量大小为 1。它可以是 tf 类型。张量 4D、TypedArray 或数组。
*   **过滤器尺寸:**所述形状的过滤器尺寸:【过滤器高度，过滤器宽度】。在这种情况下，过滤器大小是一个单数，那么 filterHeight == filterWidth。它可以是类型[数字，数字]或数字。
*   **步幅:**形状池的规定步幅:【条纹，条纹】。在这种情况下，跨步是一个单数，那么 strideHeight = = strideWidth。它可以是类型[数字，数字]或数字。
*   **填充:**所述的填充算法类型。它可以是有效类型、相同类型或数字类型。
    *   这里，对于相同和步长 1，输出将具有与输入相同的大小，而与滤波器大小无关。
    *   对于“有效”，在滤波器尺寸大于 1*1×1 的情况下，输出应小于输入。
*   **includebatchindex:**可选，类型为布尔值。

**返回值:**返回{[名称:字符串]: tf。张量}。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining input tensor
const x = tf.tensor4d([1, 2, 3, 4], [2, 2, 1, 1]);

// Calling maxPoolWithArgmax() method
const result = tf.maxPoolWithArgmax(x, 3, 2, 'same');

// Printing output
console.log(result)
```

**输出:**

```
{
  "result": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [
      2,
      1,
      1,
      1
    ],
    "dtype": "float32",
    "size": 2,
    "strides": [
      1,
      1,
      1
    ],
    "dataId": {
      "id": 20
    },
    "id": 20,
    "rankType": "4",
    "scopeId": 14
  },
  "indexes": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [
      2,
      1,
      1,
      1
    ],
    "dtype": "float32",
    "size": 2,
    "strides": [
      1,
      1,
      1
    ],
    "dataId": {
      "id": 21
    },
    "id": 21,
    "rankType": "4",
    "scopeId": 14
  }
}
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling maxPoolWithArgmax() method
console.log(tf.maxPoolWithArgmax(
    tf.tensor4d([1.1, 2.1, 3.1, 4.1], 
    [1, 2, 2, 1]), [1, 2], [1, 1], 
    'valid', true
));
```

**输出:**

```
{
  "result": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [
      1,
      2,
      1,
      1
    ],
    "dtype": "float32",
    "size": 2,
    "strides": [
      2,
      1,
      1
    ],
    "dataId": {
      "id": 80
    },
    "id": 80,
    "rankType": "4",
    "scopeId": 54
  },
  "indexes": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [
      1,
      2,
      1,
      1
    ],
    "dtype": "float32",
    "size": 2,
    "strides": [
      2,
      1,
      1
    ],
    "dataId": {
      "id": 81
    },
    "id": 81,
    "rankType": "4",
    "scopeId": 54
  }
}
```

**参考资料:**[https://js . tensorlow . org/API/latest/# maxpoolwithargmax](https://js.tensorflow.org/api/latest/#maxPoolWithArgmax)