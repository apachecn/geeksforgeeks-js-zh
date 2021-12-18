# tensorlow . js TF . image . cropandresize()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-image-cropandresize-function/

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**image . cropandresize()函数**用于从所述输入图像张量中取出输出，并通过双线性采样或最近邻采样将其重新缩放至由裁剪长度所述的正常输出维度。

**语法:**

```
tf.image.cropAndResize(image, boxes, boxInd, cropSize, 
method?, extrapolationValue?)
```

**参数:**该方法接受以下参数:

*   **图像:**所述的 4d 张量，其具有配置[批次、图像高度、图像宽度、深度]。其中，*图像高度*以及*图像宽度*应该为正，定义要拍摄作物的图像组。它可以是 tf 类型。张量 4D、TypedArray 或数组。
*   **框:**所述的 2d 浮体 32 张量，其具有构型[numBoxes，4]。并且每次访问都是[y1，x1，y2，x2]，允许(y1，x1)和(y2，x2)是该组中 boxInd[i]图像中框的标准化坐标。它可以是 tf 类型。张量 2D、TypedArray 或数组。
*   **boxInd:** 所述 1d int32 张量，其具有配置[numBoxes]以及范围[0，batch 中的值，该范围定义了第 I 个框指示的图像。它是 tf 类型的。张量 1、类型 1 或数组。
*   **cropSize:** 是所述的 1d int32 张量，它有两个元素，并且具有定义每种作物被重新缩放到的长度的构型[crophehigh，cropWidth]。它是类型[数字，数字]。
*   **方法:**它是一个可选参数，用于定义重新缩放的采样方法。默认值为*双线性*。它可以是“双线性”或“最近”类型。
*   **外推值:**是规定的阈值，用于根据规定的分数推断何时删除方框。默认值为零。它是可选的，并且是数字类型。

**返回值:**返回 tf。张量 4D 对象。

**示例 1:** 使用 4d 张量、方块、装箱数和 cropSize 参数。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs")

// Calling image.cropAndResize() method and
// Printing output
tf.image.cropAndResize(tf.tensor4d([[
  [[1, 7], [21, 9]],
  [[8, 9], [1, 33]]
]]), tf.tensor2d([1, 2, 3, 4], [1, 4]), [2], [1, 1]).print();
```

**输出:**

```
Tensor
     [ [ [[0, 0],]]]
```

**示例 2:** 使用浮点数组、方法和外推值。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs")

// Defining an array of floats
const arr = [[
  [[1.1, 1.7, 1.5, 1.1], 
  [1.7, 1.9, 8.1, 6.3]],
  [[3.3, 3.4, 3.7, 4.0], 
  [5.1, 5.2, 5.3, 5.9]]
]];

// Defining boxes with an array of floats
const boxes = [[11.1, 2.3, 7.3, 6.4], [1, 4]];

// Calling image.cropAndResize() method and
// Printing output
tf.image.cropAndResize(arr, boxes, [2, 4], [2, 1], 'nearest', 0.4).print();
```

**输出:**

```
Tensor
    [[ [[0, 0, 0, 0],],

       [[0, 0, 0, 0],]],

     [ [[0, 0, 0, 0],],

       [[0, 0, 0, 0],]]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#image.cropAndResize