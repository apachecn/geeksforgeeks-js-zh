# tensorflow . js . TF . layers computeOutputShape()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-computeoutputshape-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-computeoutputshape-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。computeOutputShape()函数**用于枚举所述图层的输出形状。并且假定将创建该层，以便与所提供的输入形状相匹配。

**语法:**

```
computeOutputShape(inputShape)
```

**参数:**

*   **输入形状:**是指定的形状，即一组整数或一组形状的列表。此外，*形状*元组可以包含有利于自由大小的空位，以代替整数。它的类型可以是((null | number)[]|(null | number)[][])。

**返回值:**返回(空|数)[]|(空|数)[][]。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding a layer
model.add(tf.layers.dense({units: 1, inputShape: [3]}));

// Defining inputShape
const inputShape = [6, 2, 6];

// Calling computeOutputShape() method with its 
// parameter
const val = model.layers[0].computeOutputShape(inputShape);

// Printing output
console.log(val);
```

**输出:**

```
6,2,1
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding layers
model.add(tf.layers.dense({units: 1, inputShape: [3]}));
model.add(tf.layers.dense({units: 5}));

// Defining inputShape
const inputShape1 = [6, 2, 6, null];
const inputShape2 = [6.5, 2.6, 9.1, NaN];

// Calling computeOutputShape() method with its 
// parameter
const val1 = model.layers[0].computeOutputShape(inputShape1);
const val2 = model.layers[1].computeOutputShape(inputShape2);

// Printing output
console.log(val1);
console.log(val2);
```

**输出:**

```
6,2,6,1
6.5,2.6,9.1,5
```

**参考:**[https://js . tensorflow . org/API/latest/# TF . layers . layer . computeoutputshape](https://js.tensorflow.org/api/latest/#tf.layers.Layer.computeOutputShape)