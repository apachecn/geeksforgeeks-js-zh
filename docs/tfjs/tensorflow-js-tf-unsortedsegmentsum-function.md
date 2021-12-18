# tensorlow . js TF . unsortedsesegmentsum()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-unsortedsegmentsum-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-unsortedsegmentsum-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。unsortedSegmentSum()函数**用于计算一个 tf.Tensor 的各部分之和。

**语法:**

```
tf.unsortedSegmentSum(x, segmentIds, numSegments)
```

**参数:**

*   **x:** 它是通过其各部分相加的所述张量输入，并且它可以是 tf 类型。张量、类型或数组。
*   **段号:**是规定的 tf。张量 1D，其阶等于 x 穿过轴的大小的阶。它将 *x* 的每个项目映射到一个切片。它可以是 tf 类型。张量 1、类型 1 或数组。
*   **段号:**是单独的*段号的规定编号，*是类型号。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input, segmentIds 
// and numSegments 
const y = tf.tensor1d([5, 6, 7, 8]);
const segmIds = tf.tensor1d([3, 1, 2, 0], 'int32');
const numSegm = 4;

// Calling tf.unsortedSegmentSum() method
// And printing output
y.unsortedSegmentSum(segmIds, numSegm).print();
```

**输出:**

```
Tensor
    [8, 6, 7, 5]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling tf.unsortedSegmentSum() method
var res = tf.unsortedSegmentSum(
    tf.tensor1d([1, 9]), 
    tf.tensor1d([1, 0], 'int32'), 3
);

// Printing output
res.print();
```

**输出:**

```
Tensor
    [9, 1, 0]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#unsortedSegmentSum