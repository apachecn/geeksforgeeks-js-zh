# tensorflow . js TF . regulators . L1()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-regulators-L1-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-regularizers-l1-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**正则化 l1()函数**用于 L1 正则化。此外，为了斥责巨大的权重，它在损失后面加上了一个名字:损失+= sum(l1 * abs(x))。

**语法:**

```
tf.regularizers.l1(config?)
```

**参数:**

*   **配置:**是可选对象。它下面是 l1。
*   **l1:** 是所述的 l1 正则化率，其默认值为 0.01。它是数字类型的。

**返回值:**返回*正则化器*。

**示例 1:** 在本例中，我们将看到 l1 正则化器独立应用于核权重矩阵。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs");

// Define sequential model
const model = tf.sequential();

// Adding layer to it and calling 
// regularizers.l1() method
model.add(tf.layers.dense({
    units: 37, batchInputShape:[null, 40],
    kernelRegularizer:tf.regularizers.l1()
}));

// Calling summary() method and 
// Printing output
model.summary();
```

**输出:**

```
_________________________________________________________________
Layer (type)                 Output shape              Param #   
=================================================================
dense_Dense52 (Dense)        [null,37]                 1517      
=================================================================
Total params: 1517
Trainable params: 1517
Non-trainable params: 0
_________________________________________________________________
```

**示例 2:** 在本例中，我们将看到 l1 正则化器独立应用于偏置向量。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs");

// Define sequential model
const model = tf.sequential();

// Adding layer to it and calling 
// regularizers.l1() method
model.add(tf.layers.dense({
    units: 2, batchInputShape:[null, 13],
    biasRegularizer:tf.regularizers.l1()
}));

// Calling summary() method and 
// Printing output
model.summary();
```

**输出:**

```
_________________________________________________________________
Layer (type)                 Output shape              Param #   
=================================================================
dense_Dense54 (Dense)        [null,2]                  28        
=================================================================
Total params: 28
Trainable params: 28
Non-trainable params: 0
_________________________________________________________________
```

**参考:**T2】https://js.tensorflow.org/api/latest/#regularizers.l1