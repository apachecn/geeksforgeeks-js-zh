# tensorlow . js TF . image . non maxsuppressionpaddedsync()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-image-non maxsuppressionpaddedsync-function/

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**. image . nonmaxsuppressionpaddesync()函数**用于根据 iou 异步执行限制框的非最大值抑制，即交集超过并集以及填充结果的机会。

**语法:**

```
tf.image.nonMaxSuppressionPaddedAsync(boxes, scores, maxOutputSize, 
    iouThreshold?, scoreThreshold?, padToMaxOutputSize?)
```

**参数:**

*   **框:**所述的二维张量，其具有构型[numBoxes，4]。并且每个访问都是[y1，x1，y2，x2]，允许(y1，x1)和(y2，x2)是限制框的边缘。它可以是 tf 类型。张量 2D、TypedArray 或数组。
*   **分数:**所述的 1d 张量，前提是方框分数是配置[numBoxes]。它是 tf 类型的。张量 2D、TypedArray 或数组。
*   **最大输出尺寸:**是所述的要被挑选的箱子的最大数量。它是数字类型的。
*   **借条阈值:**是表示阈值的所述浮动，以便决定所述框是否与借条相交过多。应该在[0，1]中间。默认值为 0.5，即 50%的方块相交。它是可选的，并且是数字类型。
*   **分数阈值:**这是规定的阈值，以便根据规定的分数决定何时移除箱子。缺省值是-inf，也就是说，允许每一个分数。它是可选的，并且是数字类型。
*   **padToMaxOutputSize:** 是布尔类型的可选参数。默认值为*假*。如果是真的，那么结果*选择的维度*被填充到*最大输出尺寸*。

**返回值:**返回{[名称:字符串]: tf 的承诺。张量}。

**示例 1:** 在本例中，我们将使用 2d 张量、分数和 maxOutputSize 参数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs";

// Calling image.nonMaxSuppressionPaddedAsync() method
const output = await tf.image.nonMaxSuppressionPaddedAsync(
  tf.tensor2d([1, 2, 3, 4, 2, 4, 6, 7], [2, 4]), [1, 1], 4 );

// Printing output
console.log(output);
```

**输出:**

```
{
  "selectedIndices": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [2],
    "dtype": "int32",
    "size": 2,
    "strides": [],
    "dataId": {
      "id": 54
    },
    "id": 54,
    "rankType": "1",
    "scopeId": 27
  },
  "validOutputs": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [],
    "dtype": "int32",
    "size": 1,
    "strides": [],
    "dataId": {
      "id": 55
    },
    "id": 55,
    "rankType": "0",
    "scopeId": 27
  }
}

```

**示例 2:** 在本例中，我们将使用浮点、iouThreshold、scoreThreshold 以及 padToMaxOutputSize 的数组。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs";

// Defining an array of floats
const arr = [
  [11.1, 2.3, 7.3, 6.4], [3, 6]]

// Calling image.nonMaxSuppressionPaddedAsync() method
const res = await tf.image.nonMaxSuppressionPaddedAsync(
  arr, [2.1, 0], 100, 0.5, 1, true);

// Printing output
console.log(res);
```

**输出:**

```
{
  "selectedIndices": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [2],
    "dtype": "int32",
    "size": 2,
    "strides": [],
    "dataId": {
      "id": 62
    },
    "id": 62,
    "rankType": "1",
    "scopeId": 29
  },
  "validOutputs": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [],
    "dtype": "int32",
    "size": 1,
    "strides": [],
    "dataId": {
      "id": 63
    },
    "id": 63,
    "rankType": "0",
    "scopeId": 29
  }
}

```

**参考:**T2