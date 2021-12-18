# Tensorflow.js tf。张量类。数组()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-tensor-class-array-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-class-array-method/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**。array()方法**用于像嵌套数组一样返回张量输入。此外，数据的重新定位是异步进行的。

**语法:**

```
array()
```

**参数:**此方法不保存任何参数。

**返回值:**返回数字[]的承诺。

**例 1:**

## Javascript

```
// Importing tensorflow library
import * as tf from "@tensorflow/tfjs"

// Creating a tensor
const tn = tf.tensor([5, 6, 3, 4]);

// Calling array() method
const res = await tn.array();

// Printing output
console.log(res)
```

**输出:**

```
5,6,3,4
```

**例二:**

## Javascript

```
// Importing tensorflow library
import * as tf from "@tensorflow/tfjs"

// Calling array() method and
// Printing output
console.log(await tf.tensor2d([1.7, 3.7, 9.7, null], [4, 1]).array());
```

**输出:**

```
1.7000000476837158,3.700000047683716,9.699999809265137,0
```

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.Tensor.array