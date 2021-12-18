# tensorflow . js TF . stridedslice()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-strided slice-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-stridedslice-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。stridedSlice()函数**用于拉出所述输入张量的条纹部分。

**注意:** <该功能用于从所述输入张量中拉出所述长度*步幅*的一部分。从*给定的位置开始*，在所有测量值大于*结束*之前，切片通过将步幅附加到所述索引来进行。此外，步幅也可以是负的，这导致反向切片。

**语法:**

```
tf.stridedSlice(x, begin, end, strides?, beginMask?, endMask?, 
ellipsisMask?, newAxisMask?, shrinkAxisMask?)
```

**参数:**

*   **X:** The tensor is a step slice. It can be tf type. Tensor, type or array.
*   **Start:** The specified coordinates from the slice. It is the type numbered [].
*   **End:** The designated coordinates of the end of the slice. It is the type numbered [].
*   **stride:** The specified length of the slice. It is optional and of type number [].
*   **beginmask:** is an optional parameter, type number. In this case, the ith bit of beginMask is fixed, then begin[i] is ignored, on the contrary, the maximum range that can be reached in this dimension is utilized.
*   **endmask:** is an optional parameter, type number. In this case, the ith bit of the endMask is fixed, so the end[i] is ignored, on the contrary, the maximum range that can be reached in this dimension is utilized.
*   **ellipsis mask:** is an optional parameter of the type number.
*   **newaxismask:** is an optional parameter of the type number.
*   **Shrinkage mask: the bit mask described in** , in which bit *I* indicates that ith specifies that the capacity must be shrunk. *Start* and *End* should indicate the size of a piece of length 1\. It is optional and of numeric type.

**返回值:**返回 tf.Tensor

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input
const tn = tf.tensor3d([5, 5, 5 ,7, 7, 7, 13, 
    13, 13, 14, 14, 14, 1, 1, 1, 2, 2, 2],
    [3, 3, 2]);

// Calling stridedSlice() method and 
// Printing output
tn.stridedSlice([5, 0, 5], [7, 5, 7], [2, 2, 2]).print();
```

**输出:**

```
Tensor
    [[[1],
      [2]]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input
const tn = tf.tensor3d([5, 5, 5 ,7, 7, 7, 13, 
    13, 13, 14, 14, 14, 1, 1, 1, 2, 2, 2],
    [3, 3, 2]);

// Defining all the parameters
const x = [-5, 5, 7];
const begin = [-7, 13, 14];
const end = [-7, 13, 13];
const strides = [1];
const beginMask = 2;
const endMask = 0;
const ellipsisMask = 2;
const shrinkAxisMask = 15;

// Calling stridedSlice() method and 
// Printing output
tn.stridedSlice(x, begin, end, strides, beginMask,
     endMask, ellipsisMask, shrinkAxisMask).print();
```

**输出:**

```
Tensor
    2
```

**参考:**T2】https://js.tensorflow.org/api/latest/#stridedSlice