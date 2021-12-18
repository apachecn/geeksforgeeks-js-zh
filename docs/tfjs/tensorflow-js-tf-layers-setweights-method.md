# tensorflow . js . TF . layers setWeights()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-set weights-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-setweights-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。设置权重()方法**用于根据给定的张量设置所述层的权重。

**语法:**

```
setWeights(weights)
```

**参数:**

*   **权重:**是输入张量的指定列表。它是 tf 类型的。张量[]。其中，阵列的数量及其形状应等于所用层的规定重量的尺寸数量。换句话说，它必须等于 *getWeights()* 方法的结果。

**返回值:**返回 void。

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
model.layers[0].setWeights([tf.truncatedNormal([11, 2]), tf.zeros([2])]);

// Compiling the model
model.compile({loss: 'categoricalCrossentropy', optimizer: 'sgd'});

// Printing output using getWeights() method
model.layers[0].getWeights()[0].print();
```

**输出:**

```
Tensor
    [[-0.5969906, -0.1883931],
     [0.8569255 , -0.49416  ],
     [0.1157023 , 0.1150239 ],
     [-0.4052143, 1.9936075 ],
     [0.3090054 , 0.7212474 ],
     [0.4626641 , -0.7287846],
     [0.4352857 , -0.5195332],
     [0.4626429 , 0.0216295 ],
     [-0.1110666, -0.5997615],
     [-0.5083916, -0.3582681],
     [-0.2847465, 1.184485  ]]
```

这里，使用*截断法线()*方法来创建 tf。张量连同从截断正态分布采样的值一起，使用*零点()*方法来创建 tf。张量以及设置为 0 的所有元素和*获取权重()*方法用于打印使用*设置权重()*方法设置的权重。

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

// Printing output using getWeights() method
model.layers[0].getWeights()[0].print();
model.layers[0].getWeights()[1].print();
model.layers[1].getWeights()[0].print();
model.layers[1].getWeights()[1].print();
```

**输出:**

```
Tensor
    [[1],
     [1],
     [1],
     [1],
     [1]]
Tensor
    [0]
Tensor
     [[1, 1],]
Tensor
    [0, 0]
```

这里，使用*one()*方法来创建 tf。张量以及设置为 1 的所有元素。

**参考:**[https://js . tensorflow . org/API/latest/# TF . layers . layer . setweights](https://js.tensorflow.org/api/latest/#tf.layers.Layer.setWeights)