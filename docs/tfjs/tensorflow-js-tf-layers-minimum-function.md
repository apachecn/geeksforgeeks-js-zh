# tensorflow . js TF . layers . minimum()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-minimum-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-minimum-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**tf.layers.minimum()** 函数用于创建一个层，该层用于计算输入数组的元素式最小值。它将具有相同形状的张量列表作为输入。

**语法:**

```
tf.layers.minimum (args)
```

**参数:**

它接受一个对象作为输入:args (Object)。提供 args 对象作为输入是可选的。以下是您可以在 args 对象中提供的字段。

*   **Input shape ((empty or numeric) []):** Create an input layer inserted before this layer.
*   **batchInputShape ((null or number) []):** has the same purpose as the above parameters, but if both the input shape and batchInputShape have been defined, batchinputshape is preferred.
*   **Batch size (number):** If the above two parameters are not specified, use batchInputShape to construct batchInputShape.
*   **Data type:** The data type of the layer. E.g. float32, int32, etc.
*   **Name (string):** is used to name the layer.

**权重(tf。Tensor[]):** 

*   **Trainable (Boolean):** is used to specify whether the weight can be updated by fitting. The default value is true.

**返回值:**返回元素方向的最小值。

**例 1:**

## Javascript

```
const tf = require("@tensorflow/tfjs")

// providing input
const x = tf.input({shape: [4, 4, 4]});
const y = tf.input({shape: [4, 4, 4]});

// creating required layer
const minimumLayer = tf.layers.minimum();
const minimum = minimumLayer.apply([x, y]);
console.log(minimum.shape);
```

**输出:**

```
[ null, 4, 4, 4 ]
```

**例 2:**

在本例中，我们将提供 args 对象作为输入，其字段为**名称**和**可训练**。

## Javascript

```
const tf = require("@tensorflow/tfjs")

// providing input
const x = tf.input({shape: [5, 5, 5]});
const y = tf.input({shape: [5, 5, 5]});
const z = tf.input({shape: [5, 5, 5]});

// creating required layer
const minimumLayer = tf.layers.minimum({name:"layer1", trainable:false});
const minimum = minimumLayer.apply([x, y, z]);
console.log(minimumLayer.name)
console.log(minimumLayer.trainable)
console.log(minimumLayer.shape);
```

**输出:**

```
layer1
false
[ null, 5, 5, 5 ]
```

**参考**:[https://js.tensorflow.org/api/latest/#minimum](https://js.tensorflow.org/api/latest/#minimum)