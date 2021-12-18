# tensorlow . js TF . logical not()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-logicalnot-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-logicalnot-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.logicalNot()** 函数用于返回布尔值张量，作为对指定布尔值张量进行元素非运算的结果。

**语法:**

```
tf.logicalNot(a, b)
```

**参数:**该函数接受两个参数，如下图所示:

*   **a:** 第一个输入张量。它应该有一个布尔数据类型。
*   **b:** 第二个输入张量。它必须具有布尔数据类型。

**返回值:**它返回一个布尔值张量，作为对指定的布尔值张量进行元素非运算的结果。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing some tensors of boolean values
const a = tf.tensor1d([false, true], 'bool');
const b = tf.tensor1d([true, false], 'bool');

// Calling the .logicalNot() function
a.logicalNot().print();
b.logicalNot().print();
```

**输出:**

```
Tensor
   [true, false]
Tensor
   [false, true]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using tensors of boolean values as
// the parameters of .logicalNot() function
tf.tensor1d([false, false], 'bool').logicalNot().print();
tf.tensor1d([true, true], 'bool').logicalNot().print();
```

**输出:**

```
Tensor
   [true, true]
Tensor
   [false, false]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#logicalNot