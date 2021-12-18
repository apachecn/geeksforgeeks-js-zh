# tensorlow . js TF . logical heat()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-logicalor-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-logicalor-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**TF . logicalol()**函数用于返回布尔值张量，该张量是对两个指定的布尔值张量进行元素或运算的结果。

**语法:**

```
tf.logicalOr(a, b)
```

**参数:**该函数接受两个参数，如下图所示:

*   **a:** 第一个输入张量。它应该有一个布尔数据类型。
*   **b:** 第二个输入张量。它应该有一个布尔数据类型。

**返回值:**返回两个指定的布尔值张量的元素或运算结果的布尔值张量。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing some tensors of boolean values
const a = tf.tensor1d([false, true], 'bool');
const b = tf.tensor1d([true, false], 'bool');

// Calling the .logicalOr() function
a.logicalOr(b).print();
```

**输出:**

```
Tensor
   [true, true]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using tensors of boolean values as
// the parameters of .logicalOr() function
tf.tensor1d([false, true, false, true], 'bool').logicalOr(
tf.tensor1d([false, true, true, false], 'bool')).print();
```

**输出:**

```
Tensor
   [false, true, true, true]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#logicalOr