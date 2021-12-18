# Tensorflow.js tf.gather()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-collect-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-gather-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。聚集()** **功能**用于根据所述索引从所述张量 x 轴收集碎片。

**语法:**

```
tf.gather(x, indices, axis?, batchDims?)
```

**参数:**

*   **x:** 是所述的要采集其碎片的输入张量，可以是 tf 类型。张量、类型或数组。
*   **指数:**是要拉出的数值的规定指数，可以是 tf 型。张量、类型或数组。
*   **轴:**是所述轴，在该轴上选择数值。默认情况下，该值为零，并且是数字类型。但是，该参数是可选的。
*   **批次尺寸:**是规定的批次尺寸数量，应小于或等于规定的等级，即指数。它的缺省值为零。此外，返回的输出必须具有 x . shape[:axis]+indexs . shape[batchDims:]+x . shape[axis+1:]的形状。它是数字类型，是可选的。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input and indices
const y = tf.tensor1d([1, 6, 7, 8]);
const ind = tf.tensor1d([1, 6, 2], 'int32');

// Calling tf.gather() method and
// Printing output
y.gather(ind).print();
```

**输出:**

```
Tensor
    [6, NaN, 7]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input, indices, axis,
// and batchdims
const y = tf.tensor2d([7, 8, 12, 13], [4, 1]);
const ind = tf.tensor1d([2, 3, 0], 'int32');
const axis = 1;
const batchdims = -1;

// Calling tf.gather() method
var res = tf.gather(y, ind, axis, batchdims);

// Printing output
res.print();
```

**输出:**

```
Tensor
    [[12 , 13 , 7 ],
     [13 , NaN, 8 ],
     [NaN, NaN, 12],
     [NaN, NaN, 13]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#gather