# tensorflow . js TF . regulators . l1l 2()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-regulators-l1l 2-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-regularizers-l1l2-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**正则化 l1l2()函数**用于 L1 和 l2 正则化。此外，它在损失后面加上一个名字，以斥责巨大的权重:损失+=总和(l1 * abs(x)) +总和(l2 * x^2).)

**语法:**

```
tf.regularizers.l1l2(config?)
```

**参数:**

*   **配置:**是可选对象。下面是 l1 和 l2。
*   **l1:** 是所述的 l1 正则化率，其默认值为 0.01。它是数字类型的。
*   **l2:** 是所述的 l2 正则化率，其缺省值为 0.01。它是数字类型的。

**返回值:**返回正则。

**示例 1:** 在本例中，我们将看到 l1l2 正则化器独立应用于核权重矩阵。

## Javascript

```
// Importing the tensorflow.js library
//const tf = require("@tensorflow/tfjs");

// Define sequential model
const model = tf.sequential();

// Adding layer to it and calling 
// regularizers.l1l2() method
model.add(tf.layers.dense({
    units: 11, batchInputShape:[3, 4],
    kernelRegularizer:tf.regularizers.l1l2()
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
dense_Dense57 (Dense)        [3,11]                    55        
=================================================================
Total params: 55
Trainable params: 55
Non-trainable params: 0
_________________________________________________________________
```

**示例 2:** 在本例中，我们将看到 l1l2 正则化器独立应用于偏置向量。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs");

// Define sequential model
const model = tf.sequential();

// Adding layer to it and calling 
// regularizers.l1l2() method
model.add(tf.layers.dense({
    units: 12, inputShape:[null, 8, 2],
    biasRegularizer:tf.regularizers.l1l2()
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
dense_Dense69 (Dense)        [null,null,8,12]          36        
=================================================================
Total params: 36
Trainable params: 36
Non-trainable params: 0
_________________________________________________________________
```

**参考:**T2】https://js.tensorflow.org/api/latest/#regularizers.l1l2