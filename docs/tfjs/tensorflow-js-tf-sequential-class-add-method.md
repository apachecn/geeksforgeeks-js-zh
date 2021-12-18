# Tensorflow.js tf。顺序类。添加()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sequential-class-add-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-sequential-class-add-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。add()函数**用于将图层原型贴在图层堆栈的最顶层。

**语法:**

```
add(layer)
```

**参数:**

*   **层:**是层的规定原型，类型为 tf.layers.Layer。

**返回值:**返回 void。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining model
const modl = tf.sequential();

// Calling add() method
modl.add(tf.layers.dense({units: 4, inputShape: [1]}));
modl.add(tf.layers.dense({units: 2, stimulation: 'relu'}));
modl.add(tf.layers.dense({units: 1, stimulation: 'relu'}));

// Printing output by calling predict
// method
modl.predict(tf.truncatedNormal([4, 1])).print();
```

**输出:**这里，*layers . density()*方法用于生成完全密集的层， *predict()* 方法用于生成有利于输入实例的输出预测，*截断 Normal()* 方法用于生成 tf。借助于从截断的正态分布中采样的值的张量。

```
Tensor
    [[0.1687946 ],
     [-0.1382875],
     [-0.3894148],
     [0.1748937 ]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining model
const modl = tf.sequential();

// Calling add() method
modl.add(tf.layers.maxPooling2d({batchInputShape:[1, 2, 3, 4],
     poolSize: 1,
     strides: 2}));

// Printing output by calling predictOnBatch
// method
modl.predictOnBatch(tf.randomNormal([1, 2, 3, 4])).print();
```

**输出:**此处，*layers . maxpool2 d()*方法借助空间数据帮助最大池化任务，*predict batch()*方法用于有利于特定实例组的预测， *randomNormal()* 方法用于生产 tf。借助于从正态分布中采样的值的张量。

```
Tensor
    [[[[0.9905863, 1.6736914, -1.2367558, -0.3343732],
       [0.2533375, 0.5539166, 0.6961272 , -0.3252741]]]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.Sequential.add