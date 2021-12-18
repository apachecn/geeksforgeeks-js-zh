# tensorflow . js TF . regulators . L2()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-regulators-L2-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-regularizers-l2-function/)

Tensorflow.js 中的 Regularisers 与模型的各种组件相连接，这些组件与 score 函数一起工作，帮助驱动可训练的值，即大值。方法 TF . regulators . L2()继承自正则化类。TF . regulators . l2()方法在模型训练的惩罚情况下应用 L2 正则化。这种方法在损失中增加了一项，对大权重进行惩罚。它加上损失+=总和(l2 * x^2)损失。因此，在本文中，我们将看到 TF . regulators . L2()函数是如何工作的。

**语法:**

```
tf.regularizers.l2 (args);
```

**参数:**

*   **L2:** This number indicates that the regularization rate is 0.01 by default.

**返回:**正则化

**示例 1:** 在本例中，我们将看到 l2 正则化器独立应用于核权重矩阵。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs");

// Define sequential model
const model = tf.sequential();

// Add layer to it
model.add(tf.layers.dense({
    units: 32, batchInputShape:[null,50],
    kernelRegularizer:tf.regularizers.l2()
}));

// Model summary
model.summary();
```

**输出:**

```
Layer (type)                 Output shape              Param #   
=================================================================
dense_Dense1 (Dense)         [null,32]                 1632      
=================================================================
Total params: 1632
Trainable params: 1632
Non-trainable params: 0
```

**示例 2:** 在本例中，我们将看到 l2 正则化器独立应用于偏置向量。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs");

// Define sequential model
const model = tf.sequential();

// Add layer to it
model.add(tf.layers.dense({
    units: 32, batchInputShape:[null,50],
    biasRegularizer:tf.regularizers.l2()
}));

// Model summary
model.summary();
```

**输出:**

```
Layer (type)                 Output shape              Param #    
=================================================================
dense_Dense2 (Dense)         [null,32]                 1632      
=================================================================
Total params: 1632
Trainable params: 1632
Non-trainable params: 0
```

**参考文献:**T2】https://js.tensorflow.org/api/latest/#regularizers.l2