# Tensorflow.js tf。LayersModel 类。getLayer()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers model-class-getlayer-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layersmodel-class-getlayer-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。getLayer()函数**用于获取基于名称(必须是唯一的)或索引的图层。其中，索引依赖于自下而上的水平图遍历顺序。此外，如果同时给出*名称*和*指数*，则指数优先。

**语法:**

```
getLayer(name?, index?)
```

**参数:**

*   **名称:**是图层的声明名称。它是可选的，并且是字符串类型。
*   **指数:**是层的规定指数。它是可选的，并且是数字类型。

**返回值:**返回 tf.layers.Layer。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining model
const model = tf.sequential();

// Adding a layer
model.add(tf.layers.dense({units: 4, inputShape: [1]}));

// Calling getLayer() method
const layer_0 = model.getLayer(null, 0);

// Printing weights of the layer_0
// using getWeights() method
layer_0.getWeights()[0].print();
```

**输出:**

```
Tensor
     [[-0.0678914, 0.6647689, -0.3708572, -0.1764591],]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining model
const model = tf.sequential();

// Adding layers
model.add(tf.layers.dense({units: 4, inputShape: [1]}));
model.add(tf.layers.dense({units: 2, inputShape: [3], activation: 'relu6'}));
model.add(tf.layers.dense({units: 3, inputShape: [5], activation: 'sigmoid'}));

// Calling getLayer() method
const layer_0 = model.getLayer(NaN, 0);
const layer_1 = model.getLayer('denselayer', 1);
const layer_2 = model.getLayer(undefined, 2);

// Printing number of numbers in the weights
// of the layer_0, layer_1, and layer_2 
// using countParams() method
console.log(layer_0.countParams());
console.log(layer_1.countParams());
console.log(layer_2.countParams());
```

**输出:**

```
8
10
9
```

**参考:**[https://js.tensorflow.org/api/latest/#tf.图层模型获取图层](https://js.tensorflow.org/api/latest/#tf.LayersModel.getLayer)