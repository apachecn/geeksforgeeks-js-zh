# tensorflow . js TF . initializer . identity()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-initializer-identity-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-initializers-identity-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

初始值设定项类是 Tensorflow.js 中所有初始值设定项的基类。初始值设定项用于用特定值初始化 Tensors。它返回初始化器指定的初始化的张量对象。所以在本文中，我们将看到身份初始化器是如何工作的。这是初始化器，用一个单位矩阵初始化了一个新的张量对象。它只用于 2D 矩阵。

**语法:**

```
tf.initializers.identity(Gain)
```

**参数:**

*   **增益**:适用于单位矩阵的是乘法因子。

**返回值:**返回**初始值**

**示例 1:** 在本例中，我们将检查 identity()函数的独立使用。

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Generates the identity matrix
const value=tf.initializers.identity(1.0)

// Print gain
console.log(value)
```

**输出:**

```
{
 "gain": 1
}
```

**示例 2:** 在本例中，我们将使用 identity()和 density()函数使用具有密集层的恒等式矩阵。

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Define the input
const inp = tf.input({shape:[4]});

// Create identity matrix with gain 1
const value=tf.initializers.identity(1.0)

// Dense layer 1
const denseLayer1 = tf.layers.dense({
    units: 6,
    activation: 'relu',
    kernelInitialize: value
});

// Dense layer 2
const denseLayer2 = tf.layers.dense({
    units: 8,
    activation: 'softmax'
});

const out = denseLayer2.apply(denseLayer1.apply(inp));

//  Model creation
const model = tf.model({inputs:inp,outputs:out});

// Make prediction
console.log("Lets Make Some Prediction :")
model.predict(tf.ones([2, 4])).print();
```

**输出:**

```
Lets Make Some Prediction :
Tensor
   [[0.1651815, 0.1695402, 0.0670628, 0.0771763, 
     0.1045933, 0.1027268, 0.1647871, 0.148932],
    [0.1651815, 0.1695402, 0.0670628, 0.0771763, 
     0.1045933, 0.1027268, 0.1647871, 0.148932]]
```

**参考:**T2】https://js.tensorflow.org/api/3.6.0/#initializers.identity