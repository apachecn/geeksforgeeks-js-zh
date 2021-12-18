# Tensorflow.js tf。LayersModel 类。预测()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers model-class-predict-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layersmodel-class-predict-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

那个。**预测()函数**用于产生给定输入实例的输出估计值。此外，这里的计算是成套进行的。其中，*步骤*操作目前不支持，只需要 tensorflow.js 的核心后端。

**语法:**

```
predict(x, args?)
```

**参数:**

*   **x:** 它是规定的输入数据，就像张量一样，否则就是 tf 的数组。张量，以防模型有不同的输入。它可以是 tf 类型。张量或 tf。张量[]。
*   **args:** 是所述的拥有选择字段的 ModelPredictArgs 对象。
    1.  **批次尺寸:**是所述的批次尺寸，类型为整数。如果未定义，缺省值将是 32。
    2.  **详细:**是默认为假的陈述详细模式。

**返回值:**返回 tf。张量对象。张量[]。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining model
const Mod = tf.sequential({
   layers: [tf.layers.dense({units: 2, inputShape: [30]})]
});

// Calling predict() method and
// Printing output
Mod.predict(tf.randomNormal([6, 30])).print();
```

**输出:**

```
Tensor
    [[-0.7650393, -0.8317917],
     [-0.7274997, 1.827635  ],
     [-0.9398478, -0.2998275],
     [-1.0945926, -1.9154934],
     [0.0067322 , -1.9220339],
     [0.2052939 , 0.6488774 ]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling predict() method and
// Printing output
tf.sequential({
   layers: [tf.layers.dense({units: 3, inputShape: [10]})]
}).predict(tf.truncatedNormal([2, 10]), {batchSize: 2}, true).print();
```

**输出:**

```
Tensor
    [[0.2670097, -1.2741219, -0.3159108],
     [0.9108799, -0.1305539, -0.1370454]]
```

**参考:**[https://js.tensorflow.org/api/latest/#tf.图层模型预测](https://js.tensorflow.org/api/latest/#tf.LayersModel.predict)