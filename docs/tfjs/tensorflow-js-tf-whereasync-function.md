# tensorflow . js . TF . wheasync()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-wheasync-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-whereasync-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**函数用于返回指定条件下真元素坐标的二维张量。在返回的张量中，第一维(即行)指定真实元素的数量，第二维(即列)指定真实元素的坐标，即输出张量的形状为[numtreelems，condition.rank]。**

**注意:**返回张量的形状取决于输入中存在的真实值。

**语法:**

```
tf.whereAsync (condition)
```

**参数:**该函数接受一个参数，如下图所示:

*   **Condition:** The input condition is an array of Boolean values.

**返回值:**返回指定条件下真元素坐标的二维张量。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a tensor for conditions
const cond = tf.tensor1d([false, true, true, false, true], 'bool');

// Calling the .whereAsync() function
const result = await tf.whereAsync(cond);

// Getting the 2-D tensor of true elements
result.print();
```

**输出:**

```
Tensor
   [[1],
    [2],
    [4]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using a tensor of conditions as the
// parameter of the .whereAsync() function
const result = await tf.whereAsync(tf.tensor1d(
  [true, false, true, true, false], 'bool'));

// Getting the 2-D tensor of true elements
result.print();
```

**输出:**

```
Tensor
   [[0],
    [2],
    [3]]
```

**参考:**T2】https://js.tensorflow.org/api/1.0.0/#whereAsync