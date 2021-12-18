# tensorlow . js TF . separable conv 2d()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-separable conv 2d-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**.separableConv2d()函数**用于确定 2d 复杂度以及可分离的滤波器。它执行深度方向的*复杂度，该复杂度在通过点方向的*复杂度追求的通道上明显工作，这有助于混合通道。而且，它规定了[1，2]和 3 维内的可分性，绝对不是 1 维和 2 维内的结构可分性。**

****语法:****

```
**tf.separableConv2d(x, depthwiseFilter, pointwiseFilter, 
        strides, pad, dilation?, dataFormat?)**
```

****参数:****

*   ****x:** 所述的输入张量，其或者是等级 3 或者是等级 4，并且具有形状:【批次、高度、宽度、英寸通道】。此外，在等级为 3 的情况下，则假定批量大小为 1。它可以是 tf 类型。张量 3D，tf。张量 4D、TypedArray 或数组。**
*   ****深度方向滤波器:**所述的*深度方向*滤波器张量等级 4 和形状:【滤波器高度，滤波器宽度，通道，通道倍增器】。然而，它是在最初阶段使用的。它可以是 tf 类型。张量 4D、TypedArray 或数组。**
*   ****点态滤波器:**所述的*点态*滤波器张量等级 4 和形状:[1，1，inChannels * channelMultiplier，outChannels]。然而，它被用于操作的第二阶段。它可以是 tf 类型。张量 4D、TypedArray 或数组。**
*   ****步幅:**所述的形态复杂化的步幅:【条纹，条纹】。在这种情况下，所述步幅是一个单数，那么 strideHeight = = strideWidth。它可以是类型[数字，数字]或数字。**
*   ****填充:**所述的填充算法类型。它可以是有效类型或相同类型。

    *   这里，对于“相同”和步幅 1，输出将具有与输入相同的大小，而与滤波器大小无关。
    *   对于“有效”输出应小于输入，以防滤波器尺寸大于 1*1×1。** 
*   ****膨胀:**所述的膨胀。它是可选的，类型为[数字，数字]或数字。**
*   ****数据格式:**来自“NHWC”或“NCHW”的指定选择字符串。它指定所述输入和输出数据的数据形状。默认值为“NHWC”。此外，这里的数据按照以下顺序保存:【批次、高度、宽度、通道】。它是可选的，类型为“NHWC”。**

****返回值:**返回 tf。张量 3D 或 tf .张量 4D。**

****例 1:****

## **Javascript**

```
**// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining input tensor
const x = tf.tensor4d([1, 2, 3, 4], [1, 1, 2, 2]);

// Defining depthwise filter tensor
const y = tf.tensor4d([1, 1, 0, 4], [1, 1, 2, 2]);

// Defining pointwise filter tensor
const z = tf.tensor4d([1, 1, 0, 4], [1, 1,     4, 1]);

// Calling separableConv2d() method
const result = tf.separableConv2d(x, y, z, 2, 'valid');

// Printing output
result.print();**
```

****输出:****

```
**Tensor
     [ [ [[34],]]]**
```

****例二:****

## **Javascript**

```
**// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling separableConv2d() method
tf.separableConv2d(
    tf.tensor4d([1.1, 2.2, 3.3, 4.4], [1, 1, 2, 2]), 
    tf.tensor4d([1.2, 1.1, 0.3, 4.5], [1, 1, 2, 2]),
    tf.tensor4d([1.4, 1.6, 0.5, 4.8], [1, 1,     4, 1]),
    1, 'same', 1, 'NHWC').print();**
```

****输出:****

```
**Tensor
    [[[[51.6340065 ],
       [107.0520096]]]]**
```

****参考资料:**[https://js . tensorlow . org/API/latest/# separable conv 2d](https://js.tensorflow.org/api/latest/#separableConv2d)**