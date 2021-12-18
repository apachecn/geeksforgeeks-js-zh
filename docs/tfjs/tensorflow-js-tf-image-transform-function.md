# tensorflow . js TF . image . transform()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-image-transform-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-image-transform-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**.image.transform()函数**用于对图像应用指定的变换。

**语法:**

```
tf.image.transform(image, transforms, interpolation?, fillMode?, 
fillValue?, outputShape?)
```

**参数:**该方法接受以下参数:

*   **图像:**所述的 4d 张量，其具有配置[批次、图像高度、图像宽度、深度]。它可以是 tf 类型。张量 4D、TypedArray 或数组。
*   **变换:**所述的一个或多个射影变换矩阵。它是范围为 8 的一维张量，或者是维数为 N×8 的张量。在这种情况下，单行变换是[a0，a1，a2，b0 b1，b2，c0，c1]，随后它将输出点即(x，y)绘制成修改后的输入点即(x '，y ' =((A0 x+a1 y+a2)/k，(b0 x + b1 y + b2) / k)，其中 k = c0 x + c1 y + 1。此外，与将输入点绘制到输出点的变换相比，变换是相反的。
*   **插补:**是规定的插补方式。它可以是“最近”或“双线性”类型。它是可选的，缺省值为“最近”。
*   **填充模式:**这里，超出输入边界的指定点按照指定模式填充。该模式是可选的，可以是“常量”、“反射”、“环绕”或“最近”类型。默认值为“常量”。在“*反射*模式即(d c b a | a b c d | d c b a)中，通过在最大像素的边缘周围冥想来拉长输入。在“*常数*模式下(即 k k k | a b c d | k k k k ),通过将超出边界的每个值与相同的常数值 *k.* 一起填充来拉长输入。在“*环绕*模式下(即 a b c d | a b c d | a b c d ),通过围绕相对边缘来拉长输入。在最近的*模式下(即 a a a | a b c d | d d d d)，输入被最近的像素拉长。*
*   **填充值:**如果所述的*填充模式*为“*常数*，则该值是一个描绘要填充到边缘之外的值的浮点数。它是可选的，并且是数字类型。
*   **outputShape:** 可选，类型为【数字，数字】。

**返回值:**返回 tf。张量 4D 对象。

**示例 1:** 使用 4d 张量和 2d 张量，即变换。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs")

// Calling image.transform() method and
// Printing output
tf.image.transform(tf.tensor4d([[

  [[4, 7], [21, 9]],

  [[8, 9], [1, 33]]

]]), tf.tensor2d([1, 2, 3, 4, 5, 6, 7, 8], [1, 8])).print();
```

**输出:**

```
Tensor
    [[[[0, 0 ],
       [1, 33]],

      [[1, 33],
       [8, 9 ]]]]
```

**示例 2:** 使用一组*浮动*、*插值*、*填充模式*、*填充值*以及*输出形状*。

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

// Calling image.transform() method and
// Printing output
tf.image.transform(arr, tf.tensor2d(
    [1.3, 2.4, 3.5, 4.5, 5.1, 6.0, 7.2, 8.5], 
    [1, 8]),'bilinear', 'reflect', 2, [2, 2])
    .print();
```

**输出:**

```
Tensor
    [[[[3.3      , 3.4000001, 3.7      , 4        ],
       [4.3536587, 4.4536586, 4.6365857, 5.112195 ]],

      [[4.4178948, 4.5178947, 4.6936841, 5.1800003],
       [3.8970597, 4.0186343, 4.3869019, 4.721858 ]]]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#image.transform