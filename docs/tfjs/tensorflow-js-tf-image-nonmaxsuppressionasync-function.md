# tensorlow . js TF . image . non maxsuppressionsync()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-image-nonmaxsuppressionasync-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-image-nonmaxsuppressionasync-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**. image . nonmax suppressionasync()函数**用于在 iou 的基础上执行限界框的非最大值抑制，即交过并。此外，它的*异步*解释非最大抑制()方法。

**语法:**

```
tf.image.nonMaxSuppressionAsync(boxes, 
    scores, maxOutputSize, iouThreshold?, scoreThreshold?)
```

**参数:**

*   **框:**所述的二维张量，其具有构型[numBoxes，4]。并且每个访问都是[y1，x1，y2，x2]，允许(y1，x1)和(y2，x2)是限制框的边缘。它可以是 tf 类型。张量 2D、TypedArray 或数组。
*   **分数:**所述的 1d 张量，前提是方框分数是配置[numBoxes]。它是 tf 类型的。张量 2D、TypedArray 或数组。
*   **最大输出尺寸:**是所述的要被挑选的箱子的最大数量。它是数字类型的。
*   **借条阈值:**是表示阈值的所述浮动，以便决定所述框是否与借条相交过多。应该在[0，1]中间。默认值为 0.5，即 50%的方块相交。它是可选的，并且是数字类型。
*   **分数阈值:**这是规定的阈值，以便根据规定的分数决定何时移除箱子。缺省值是-inf，也就是说，允许每一个分数。它是可选的，并且是数字类型。

**返回值:**返回 tf.Tensor1D 的 Promise

**示例 1:** 在本例中，我们将使用 2d 张量、分数和 maxOutputSize 参数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling image.nonMaxSuppressionAsync() method
const output = await tf.image.nonMaxSuppressionAsync(
    tf.tensor2d([1, 2, 3, 4, 2, 4, 6, 7], 
    [2, 4]), [1, 1], 4);

// Printing output
output.print();
```

**输出:**

```
Tensor
    [0, 1]
```

**示例 2:** 在本例中，我们将使用一个浮点数组、iouThreshold 以及 scoreThreshold。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining an array of floats
const arr = [[11.1, 2.3, 7.3, 6.4], [3, 6]]

// Calling image.nonMaxSuppressionAsync() method
const res = await tf.image.nonMaxSuppressionAsync(
    arr, [2.1, 0], 100, 0.5, 1);

// Printing output
res.print();
```

**输出:**

```
Tensor
    [0]
```

**参考:**[https://js . tensorflow . org/API/latest/# image . nonmaxsuppressionasync](https://js.tensorflow.org/api/latest/#image.nonMaxSuppressionAsync)