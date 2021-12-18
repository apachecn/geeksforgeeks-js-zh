# tensorlow . js TF . conv 1d()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-conv 1d-function/

**简介:** Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型以及深度学习神经网络。

**. con vid()函数**用于确定所述输入张量的 1d 卷积。

**语法:**

```
tf.conv1d(x, filter, stride, pad, dataFormat?, dilation?, dimRoundingMode?)
```

**参数:**

*   **x:** 所述的输入张量，其或者是等级 3 或者等级 2，并且具有形状:【批次、高度、宽度、英寸通道】。此外，在等级为 2 的情况下，则假定批量大小为 1。它可以是 tf 类型。张量 2D，tf。张量 3D、类型数据或数组。
*   **滤波器:**所述的秩 3 的滤波器张量和形状:【滤波器高度、滤波器宽度、深度】。它可以是 tf 类型。张量 3D、类型数据或数组。
*   **步长:**规定的进气道数量，在此帮助下，规定的*过滤器*在每一步向右移动。它是数字类型的。
*   **填充:**所述的填充算法类型。它可以是有效类型、相同类型、数字类型或 conv 类型。
    1.  这里，对于相同和步长 1，输出将具有与输入相同的大小，而与滤波器大小无关。
    2.  对于“有效”，在滤波器尺寸大于 1*1×1 的情况下，输出应小于输入。
*   **数据格式:**从“NWC”或“NCW”中选择的指定字符串。缺省值为“NWC”，信息按照[批处理，in_width，in _ channels 的顺序保存。而且，只是“NWC”目前受到青睐。它是可选的，类型为“NWC”或“NCW”。
*   **膨胀:**在萎缩卷积中对输入值进行采样的规定膨胀率。默认值为 1。如果大于 1，步幅应该是 1。它是可选的，并且是数字类型。
*   **圆形模式:**从“天花板”、“圆形”或“地板”中选择的一个指定字符串。在这种情况下，如果没有提供值，则缺省值将被截断。它是可选的，类型有天花板、圆形或地板。

**返回值:**返回 tf。张量 2D 或 tf .张量 3D。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining input tensor
const x = tf.tensor3d([1, 2, 3, 4], [2, 2, 1]);

// Defining filter tensor
const y = tf.tensor3d([1, 1, 0, 4], [1, 1, 4]);

// Calling conv1d() method
const result = tf.conv1d(x, y, 2, 'valid');

// Printing output
result.print();
```

**输出:**

```
Tensor
    [ [[1, 1, 0, 4 ],],

      [[3, 3, 0, 12],]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling conv1d() method with 
// all its parameters
tf.tensor3d([1.1, 2.2, 3.3, 4.4], [2, 2, 1]).conv1d(
 tf.tensor3d([1.3, 1.2, null, -4], [1, 1, 4]),
             2, 0, 'NWC', 1, 'ceil').print();
```

**输出:**

```
Tensor
    [[[1.4299999, 1.3200001, 0, -4.4000001 ],
      [0        , 0        , 0, 0          ]],

     [[4.29     , 3.96     , 0, -13.1999998],
      [0        , 0        , 0, 0          ]]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#conv1d