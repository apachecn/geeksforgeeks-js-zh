# tensorlow . js TF . image . rotate ewithfet()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-image-rotate thoffset-function/

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**.image.rotateWithOffset()函数**用于逆时针旋转输入图像张量以及旋转的替代偏移中心。目前可以在 *CPU* 、 *WebGL* 以及 *WASM* 后端访问。

**语法:**

```
tf.image.rotateWithOffset(image, radians, fillValue?, center?)
```

**参数:**

*   **图像:**所述的 4d 张量，其具有配置[批次、图像高度、图像宽度、深度]。它可以是 tf 类型。张量 4D、TypedArray 或数组。
*   **弧度:**规定的旋转数。它是数字类型的。
*   **fillValue:** 是可选值，用于填充旋转后未使用的空位。它可以是单个的*灰度*值，即从 0 到 255，或者是三个数字的数组，即[红、绿、蓝]表示红、绿和蓝通道。默认值为零，即黑色通道。它可以是数字类型或[数字，数字，数字]。
*   **中心:**它是规定的自旋中心。它可以是一个单独的值，即从 0 到 1，也可以是两个数字的数组，即[CentreX，centerY]。默认值为 0.5。它可以是数字类型或[数字，数字]。

**返回值:**返回 tf.Tensor4D

**示例 1:** 在本例中，我们将在 tf.image.rotateWithOffset()函数中使用 4d 张量和弧度参数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling image.rotateWithOffset() method and
// Printing output
tf.image.rotateWithOffset(tf.tensor4d([[

  [[4, 7], [21, 9]],

  [[8, 9], [1, 33]]

]]), 3).print();
```

**输出:**

```
Tensor
    [[[[0, 0 ],
       [0, 0 ]],

      [[0, 0 ],
       [1, 33]]]]
```

**示例 2:** 在本例中，我们将使用一个浮点数组、fillValue 以及 center。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining an array of floats
const arr = [[

  [[1.1, 1.7, 1.5, 1.1],
  [1.7, 1.9, 8.1, 6.3]],
  [[3.3, 3.4, 3.7, 4.0],
  [5.1, 5.2, 5.3, 5.9]]

]];

// Calling image.rotateWithOffset() method and
// Printing output
tf.image.rotateWithOffset(arr, 5, [1, 2, 3], [1, 1]).print();
```

**输出:**

```
Tensor
    [[[[1, 2, 3, 3],
       [1, 2, 3, 3]],

      [[1, 2, 3, 3],
       [1, 2, 3, 3]]]]
```

**参考:**[https://js . tensorflow . org/API/latest/# image . rotatewithoffset](https://js.tensorflow.org/api/latest/#image.rotateWithOffset)