# tensorflow . js TF . layers . gaussiannoise()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-gaussiannoise-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-gaussiannoise-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

函数用于应用加性零中心高斯噪声。因为它是正则化层，所以只在训练时有效。

```
tf.layers.gaussianNoise(arguments)
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

**返回值:**返回高斯型。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing the tensor
const geek= tf.tensor1d([28561, 53678, 21343, 81422]);

// Reshaping tensor
const geek1 = tf.reshape(geek,[2,2]);

// Creating gaussianNoise of poolSize 2*2
const gaussianNoise = 
      tf.layers.gaussianNoise({poolSize:[2,2]});

// Applying gaussianNoise on geek1 tensor
const result = gaussianNoise.apply(geek1);

// Printing the result tensor
result.print();
```

**输出:**

```
Tensor
    [[28561, 53678],
     [21343, 81422]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Reshaping tensor
const geek1 = tf.reshape(
  tf.tensor1d([215, 637, 172, 368]),
  [2,2]);

// Applying gaussianNoise on geek1 tensor
tf.layers.gaussianNoise(
  {
    poolSize:[2,2]
  }
).apply(
  geek1).print();
```

**输出:**

```
Tensor
    [[215, 637],
     [172, 368]]
```

**参考资料:**[https://js . tensorlow . org/API/3 . 6 . 0/# layers . Gaussian isian/](https://js.tensorflow.org/api/3.6.0/#layers.gaussianNoise)