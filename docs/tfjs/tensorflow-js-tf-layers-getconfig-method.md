# tensorflow . js TF . layers getConfig()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-getconfig-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-getconfig-method/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**tf.layers getConfig()** 函数用于获取一个图层的配置。

**语法:**

```
getConfig()
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回图层的配置。

**示例 1:** 我们将在此示例中获取最小层的配置。

## Javascript

```
const tf = require("@tensorflow/tfjs")

// Creating a minLayer
const minLayer = tf.layers.minimum();

// Getting the configuration of the layer
const config = minLayer.getConfig();
console.log(config)
```

**输出:**

```
{ name: 'minimum_Minimum1', trainable: true }
```

**例 2:** 我们将得到这个例子中密集层的配置。

## Javascript

```
const tf = require("@tensorflow/tfjs")

// Creating a minLayer
const denseLayer = tf.layers.dense({units: 1});

// Getting the configuration of the layer
const config = denseLayer.getConfig();
console.log(config)
```

**输出:**

```
{ units: 1,
  activation: 'linear',
  useBias: true,
  kernelInitializer:
   { className: 'VarianceScaling',
     config:
      { scale: 1, mode: 'fanAvg', 
      distribution: 'normal', seed: null } },
  biasInitializer: { className: 'Zeros', config: {} },
  kernelRegularizer: null,
  biasRegularizer: null,
  activityRegularizer: null,
  kernelConstraint: null,
  biasConstraint: null,
  name: 'dense_Dense1',
  trainable: true }
```

**示例 3:** 我们将在此示例中获取应用层的配置。

## Javascript

```
const tf = require("@tensorflow/tfjs")

// Creating a minLayer
const activationLayer =
    tf.layers.activation({activation: 'relu6'});

// Getting the configuration of the layer
const config = activationLayer.getConfig();
console.log(config)
```

**输出:**

```
{ activation: 'relu6',
  name: 'activation_Activation1',
  trainable: true }
```

**参考:**[https://js . tensorflow . org/API/latest/# TF . layers . layer . getconfig](https://js.tensorflow.org/api/latest/#tf.layers.Layer.getConfig)