# tensorflow . js TF . image . nonmax suppression()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-image-nonmax suppression-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-image-nonmaxsuppression-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**.image.nonMaxSuppression()功能**用于在 *iou* 的基础上执行限界框的非最大值抑制，即交越并越。

**语法:**

```
tf.image.nonMaxSuppression(boxes, scores, 
    maxOutputSize, iouThreshold?, scoreThreshold?)
```

**参数:**

*   **框:**所述的二维张量，其具有构型[numBoxes，4]。并且每个访问都是[y1，x1，y2，x2]，允许(y1，x1)和(y2，x2)是限制框的边缘。它可以是 tf 类型。张量 2D、TypedArray 或数组。
*   **分数:**所述的 1d 张量，前提是方框分数是配置[numBoxes]。它是 tf 类型的。张量 2D、TypedArray 或数组。
*   **最大输出尺寸:**是所述的要被挑选的箱子的最大数量。它是数字类型的。
*   **借条阈值:**是表示阈值的所述浮动，以便决定所述方框是否与*借条*相交过多。应该在[0，1]中间。默认值为 0.5，即 50%的方块相交。它是可选的，并且是数字类型。
*   **分数阈值:**这是规定的阈值，以便根据规定的分数决定何时移除箱子。缺省值为 *-inf* ，即允许每个单项得分。它是可选的，并且是数字类型。

**返回值:**返回 tf.Tensor1D

**示例 1:** 在本例中，我们将使用 2d 张量、*分数*和 *maxOutputSize* 参数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling image.nonMaxSuppression() method and
// Printing output
tf.image.nonMaxSuppression(tf.tensor2d(
    [1, 2, 3, 4, 2, 4, 6, 7], 
    [2, 4]), [1, 1], 4).print();
```

**输出:**

```
Tensor
    [0, 1]
```

**示例 2:** 在本例中，我们将使用一个浮动数组， *iouThreshold* ，以及 *scoreThreshold* 。

## Javascript

```
// Importing the tensorflow.js library
//import * as tf from "@tensorflow/tfjs"

// Defining an array of floats
const arr = [[11.1, 2.3, 7.3, 6.4], [3, 6]]

// Calling image.nonMaxSuppression() method and
// Printing output
tf.image.nonMaxSuppression(arr, [2.1, 0], 100, 0.5, 1).print();
```

**输出:**

```
Tensor
    [0]
```

**参考:**[https://js . tensorflow . org/API/latest/# image . nonmax suppression](https://js.tensorflow.org/api/latest/#image.nonMaxSuppression)