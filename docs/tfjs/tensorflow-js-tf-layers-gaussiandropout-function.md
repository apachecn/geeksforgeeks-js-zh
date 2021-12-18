# tensorflow . js TF . layers . gaussiandrout()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-gaussiandrout-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-gaussiandropout-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**TF . layers . gaussiandrout()**函数用于应用乘法 1 中心高斯噪声。因为 iit 是一个正则化层，所以它只在训练时有效。

```
tf.layers.gaussianDropout(arguments)
```

**参数**

*   **Input shape:** is an optional parameter, which is used to create an input layer, and takes values such as number and null.
*   **batchinputshape:** is an optional parameter, which is used to create an input layer before the main layer, and it is equal to number and null.
*   [t0 T0】 batchSize: Its is an optional parameter for making batchInputShape, and it only accepts numbers.
*   **dtype:** is an optional parameter and represents the data type. By default, it has "float32" and other values such as "int32" and "bool" are also supported.
*   **Name:** is an optional parameter, which is used to define the layer name and accept strings.
*   **trainable** : it is an optional parameter that determines whether the provided input layer is updated or not. It accepts Boolean values.
*   **Weight:** It has the starting weight of the layer. It is also an optional parameter.
*   [T0】 input type: 【T1] is an optional parameter for inputting the data type. Like dtype, it supports all its values.

**返回值:**返回高斯和 pout。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing the tensor
const geek= tf.tensor1d([128561, 1536782, 221343, 781422]);

// Reshaping tensor
const geek1 = tf.reshape(geek,[2,2]);

// Creating gaussianDropout of poolSize 2*2
const gaussianDropout = 
      tf.layers.gaussianDropout({poolSize:[2,2]});

// Applying gaussianDropout on geek1 tensor
const result = gaussianDropout.apply(geek1);

// Printing the result tensor
result.print();
```

**输出:**

```
Tensor
    [[128561, 1536782],
     [221343, 781422 ]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Reshaping tensor
const geek1 = tf.reshape(
  tf.tensor1d([2125, 1637, 1272, 3268]),
  [2,2]);

// Applying gaussianDropout on geek1 tensor
tf.layers.gaussianDropout(
  {
    poolSize:[2,2]
  }
).apply(
  geek1).print();
```

**输出:**

```
Tensor
    [[2125, 1637],
     [1272, 3268]]
```

**参考:**T2】https://js.tensorflow.org/api/3.6.0/#layers.gaussianDropout