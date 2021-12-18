# tensorflow . js . TF . layers count params()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-count params-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-countparams-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。countParams()函数**用于查找规定权重中 *float32* 、 *int32* 等数字的绝对计数。

**语法:**

```
countParams()
```

**参数:**此方法不保存任何参数。

**返回值:**返回数字。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding a layer
model.add(tf.layers.dense({units: 2, inputShape: [11]}));

// Calling setWeights() method
model.layers[0].setWeights(
    [tf.truncatedNormal([11, 2]), tf.zeros([2])]);

// Calling countParams() method and also
// Printing output
console.log(model.layers[0].countParams());
```

**输出:**这里，*使用截断法线()*方法创建 tf。张量连同从截断正态分布采样的值一起，使用*零点()*方法来创建 tf。张量连同所有设置为 0 的元素和*设置权重()*方法用于设置权重。

```
24
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding layers
model.add(tf.layers.dense({units: 1, 
    inputShape: [5], batchSize: 1, dtype: 'int32'}));
model.add(tf.layers.dense({units: 2, inputShape: [6], batchSize: 5}));
model.add(tf.layers.dense({units: 3, inputShape: [7], batchSize: 8}));
model.add(tf.layers.dense({units: 4, inputShape: [8], batchSize: 12}));

// Calling setWeights() method
model.layers[0].setWeights([tf.ones([5, 1]), tf.zeros([1])]);
model.layers[1].setWeights([tf.ones([1, 2]), tf.zeros([2])]);

// Calling countParams() method and also
// Printing outputs
console.log(model.layers[0].countParams());
console.log(model.layers[1].countParams());
console.log(model.layers[2].countParams());
```

**输出:**这里，使用*one()*方法创建一个 tf。张量以及设置为 1 的所有元素。

```
6
4
9
```

**参考:**[https://js . tensorflow . org/API/latest/# TF . layers . layer . count params](https://js.tensorflow.org/api/latest/#tf.layers.Layer.countParams)