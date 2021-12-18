# tensorflow . js TF . depthwiseconv2d()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-depthwiseconv2d-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-depthwiseconv2d-function/)

**简介:** Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型以及深度学习神经网络。

【T0 .】深度方向卷积 2d()函数用于确定深度方向 2D 卷积。

此外，对于给定的 4D 输入阵列以及由深度为 1 的*通道*卷积滤波器组成的形状为【滤波器高度，滤波器宽度，通道数，通道数】的滤波器阵列，该方法对所有输入通道运行不同的滤波器(从 1 个通道扩展到每个通道的*通道数*通道)，然后联合连接结果。但是，输出有 inChannels *通道多个通道。

**语法:**

```
tf.depthwiseConv2d(x, filter, strides, pad, dataFormat?, 
dilations?, dimRoundingMode?)
```

**参数:**

*   **X:** The input tensor is Grade 3 or Grade 4 and has the shape: [batch, height, width, inch channel]. In addition, in the case of grade 3, it is assumed that the batch size is 1\. It can be tf type. Tensor 3D, tf. Tensor 4D, TypedArray or array.
*   **Filter: the tensor and shape of the filter with rank 4 described in** : [filter height, filter width, inChannels, channelMultiplier]. It can be tf type. Tensor 4D, TypedArray or array.
*   **stride:** The prescribed stride of convolution: [strideh8, strideWidth]. In this case, the prescribed stride length is a single number, so the strideHeight = = strideWidth. It can be of type [number, number] or number.
*   **Filling: the type of filling algorithm described in** . It can be a valid type, the same type, a numeric type or an explicit fill type.
    1.  Here, for the same and span 1, the output will have the same size as the input, regardless of the filter size.
    2.  For the case that the' effective' output should be smaller than the input, the filter size is larger than 1*1×1.
*   **Data format:** The multiple-choice character string comes from "NHWC" or "NCHW". It specifies the data format of the input and output data. The default value is "NHWC". Moreover, the data here are stored in the order of batch, height, width and channel. It is optional, which can be of type "NHWC" or "NCHW", but only "NHWC" is currently supported.
*   **Expansion:** specified expansion rate: [expansion height, expansion width] Because the input values are sampled in the height and width dimensions, it is beneficial to shrink convolution. The default value is [1,1]. In addition, if the rate is a single number, then the expansion height = = expansion width. If it is greater than 1, then all values of stride should be 1\. It is optional, and the type is [number, number], number.
*   **Inverted circular die:** The chord composed of "ceiling", "circle" or "floor". In this case, nothing is declared, so it is truncated by default. It is optional and can be floor type, round type or ceiling type.

**返回值:**返回 tf。张量 3D 或 tf .张量 4D。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining input tensor
const x = tf.tensor4d([2, 2, 3, 4], [2, 1, 1, 2]);

// Defining filter tensor
const y = tf.tensor4d([2, 1, 4, 4], [1, 1, 2, 2]);

// Calling depthwiseConv2d() method
const result = tf.depthwiseConv2d(x, y, 2, 'same');

// Printing output
result.print();
```

**输出:**

```
Tensor
    [ [ [[4, 2, 8 , 8 ],]],

      [ [[6, 3, 16, 16],]]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling depthwiseConv2d() method
tf.tensor4d([2.1, 2.2, 3.4, 4.1], [2, 1, 1, 2]).depthwiseConv2d(
 tf.tensor4d([2.1, 1.2, 4.2, 1.3], [1, 1, 2, 2]), 1, 1,
'NHWC', [1, 1], 'round').print();
```

**输出:**

```
Tensor
    [[[[0        , 0        , 0         , 0        ],
       [0        , 0        , 0         , 0        ],
       [0        , 0        , 0         , 0        ]],

      [[0        , 0        , 0         , 0        ],
       [4.4099994, 2.52     , 9.2399998 , 2.8599999],
       [0        , 0        , 0         , 0        ]],

      [[0        , 0        , 0         , 0        ],
       [0        , 0        , 0         , 0        ],
       [0        , 0        , 0         , 0        ]]],

     [[[0        , 0        , 0         , 0        ],
       [0        , 0        , 0         , 0        ],
       [0        , 0        , 0         , 0        ]],

      [[0        , 0        , 0         , 0        ],
       [7.1399999, 4.0800004, 17.2199993, 5.3299994],
       [0        , 0        , 0         , 0        ]],

      [[0        , 0        , 0         , 0        ],
       [0        , 0        , 0         , 0        ],
       [0        , 0        , 0         , 0        ]]]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#depthwiseConv2d