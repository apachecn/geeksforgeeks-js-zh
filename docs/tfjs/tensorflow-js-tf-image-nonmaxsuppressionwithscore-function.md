# tensorlow . js TF . image . non maxsuppresswithscore()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-image-non maxsuppresswithscore-function/

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**. image . nonmaxsuppressionwithscore()函数**用于在 iou 的基础上执行限界框的非最大值抑制，即交过并。此外，该操作还支持软 NMS 模式，在该模式中，框降低了不同相交框的规定分数，因此除了高分之外还支持图像的各个区域。为了启用上述软 NMS 模式，我们需要将*软 sSigma* 参数设置为大于零。

**语法:**

```
tf.image.nonMaxSuppressionWithScore(boxes, scores, maxOutputSize, 
iouThreshold?, scoreThreshold?, softNmsSigma?)
```

**参数:**

*   **框:**所述的二维张量，其具有构型[numBoxes，4]。并且每个访问都是[y1，x1，y2，x2]，允许(y1，x1)和(y2，x2)是限制框的边缘。它可以是 tf 类型。张量 2D、TypedArray 或数组。
*   **分数:**所述的 1d 张量，前提是方框分数是配置[numBoxes]。它是 tf 类型的。张量 2D、TypedArray 或数组。
*   **最大输出尺寸:**是所述的要被挑选的箱子的最大数量。它是数字类型的。
*   **借条阈值:**是表示阈值的所述浮动，以便决定所述框是否与借条相交过多。应该在[0，1]中间。默认值为 0.5，即 50%的方块相交。它是可选的，并且是数字类型。
*   **分数阈值:**这是规定的阈值，以便根据规定的分数决定何时移除箱子。缺省值是-inf，也就是说，允许每一个分数。它是可选的，并且是数字类型。
*   **softNmsSigma:** 是类型号的可选参数。这是表示有利于*软 NMS* 的西格玛参数的规定浮动。此外，如果σ为零，那么它回到*非最大抑制*。

**返回值:**返回{[名称:字符串]: tf。张量}。

**示例 1:** 在本例中，我们将使用的二维张量、分数和最大输出大小参数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling image.nonMaxSuppressionWithScore() method
const output = tf.image.nonMaxSuppressionWithScore(
    tf.tensor2d([1, 2, 3, 4, 2, 4, 6, 7], 
    [2, 4]), [1, 1], 4
);

// Printing output
console.log(output);
```

**输出:**

```
{
  "selectedIndices": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [
      2
    ],
    "dtype": "int32",
    "size": 2,
    "strides": [],
    "dataId": {
      "id": 74
    },
    "id": 74,
    "rankType": "1",
    "scopeId": 35
  },
  "selectedScores": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [
      2
    ],
    "dtype": "float32",
    "size": 2,
    "strides": [],
    "dataId": {
      "id": 75
    },
    "id": 75,
    "rankType": "1",
    "scopeId": 35
  }
}
```

**示例 2:** 在本例中，我们将使用 floats、iouThreshold、scoreThreshold 以及 softNmsSigma 的数组。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining an array of floats
const arr = [[11.1, 2.3, 7.3, 6.4], [3, 6]]

// Calling image.nonMaxSuppressionWithScore() method
const res = tf.image.nonMaxSuppressionWithScore(
    arr, [2.1, 0], 100, 0.5, 1, 0.5);

// Printing output
console.log(res);
```

**输出:**

```
{
  "selectedIndices": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [
      1
    ],
    "dtype": "int32",
    "size": 1,
    "strides": [],
    "dataId": {
      "id": 84
    },
    "id": 84,
    "rankType": "1",
    "scopeId": 42
  },
  "selectedScores": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [
      1
    ],
    "dtype": "float32",
    "size": 1,
    "strides": [],
    "dataId": {
      "id": 85
    },
    "id": 85,
    "rankType": "1",
    "scopeId": 42
  }
}
```

**参考:**T2