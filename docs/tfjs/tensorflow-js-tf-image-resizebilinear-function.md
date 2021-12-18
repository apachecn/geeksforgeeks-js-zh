# tensorflow . js TF . image .resize 双线性()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-image-resize 双线性-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-image-resizebilinear-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**image .resize 双线性()函数**用于将单个 3D 图像或一堆 3D 图像双比例缩放到不同的配置。

**语法:**

```
tf.image.resizeBilinear(images, size, alignCorners?, halfPixelCenters?)
```

**参数:**

*   **图像:**所述的等级 4 或等级 3 的图像，其具有配置[批次、高度、宽度、英寸通道]。此外，在等级 3 的情况下，则假定一个的批次。它可以是 tf 类型。张量 3D，tf。张量 4D、TypedArray 或数组。
*   **尺寸:**不同的规定配置[新高度，新宽度]，以便重新缩放图像。每个频道都被一个接一个地重新缩放。它是类型[数字，数字]。
*   **对齐参数:**是默认为假的可选参数。如果是真的，输入的大小会调整(new _ height–1)/(height–1)，这绝对会将所述图像的四个角以及重新缩放的图像进行排队。然而，如果它是假的，那么它会被新的高度/高度重新缩放。它以同样的方式处理宽度尺寸。它是类型*布尔*。
*   **半像素中心:**是默认为假的可选参数。它是类型*布尔*。

**返回值:**返回 tf。张量 3D，或 tf .张量 4D。

**示例 1:** 在本例中，我们将在 TF . image .resize 双线性()函数中使用 4d 张量和大小参数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling image.resizeBilinear() method and
// Printing output
tf.image.resizeBilinear(tf.tensor4d([[

  [[4, 7], [21, 9]],

  [[8, 9], [1, 33]]

]]), [3, 4]).print();
```

**输出:**

```
Tensor
    [[[[4        , 7        ],
       [12.5     , 8        ],
       [21       , 9        ],
       [21       , 9        ]],

      [[6.666667 , 8.333333 ],
       [7.1666665, 16.666666],
       [7.666666 , 25       ],
       [7.666666 , 25       ]],

      [[8        , 9        ],
       [4.5      , 21       ],
       [1        , 33       ],
       [1        , 33       ]]]]
```

**示例 2:** 在本例中，我们将使用一个浮点数、alignCorners 以及半像素中心的数组。

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

// Calling image.resizeBilinear() method and
// Printing output
tf.image.resizeBilinear(arr, [1, 2], true, false).print();
```

**输出:**

```
Tensor
    [[[[1.1, 1.7, 1.5      , 1.1      ],
       [1.7, 1.9, 8.1000004, 6.3000002]]]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#image.resizeBilinear