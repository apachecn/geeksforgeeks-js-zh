# tensorflow . js . TF . layers dispose()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-dispose-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-dispose-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**处置()功能**用于处置所述层的重量。此外，它通过 1 减少所述层对象的参考计数。

**注:**

*   Here, the first layer is reference counting. Among them, when its *apply ()* method is called for the first time, TF. symmetric sensor is called.
*   On the *apply ()* method, its reference number is increased by 1\. Here, when the reference number of a layer becomes zero, every weight of it will be processed, and the texture allocated in the basic memory, namely *WebGL* , will also be cleared.
*   When the reference count of the deducted layer is greater than zero, the layer weight will not be processed.
*   Finally, when a layer is disposed, it can no longer be called like *apply ()* , *getweights ()* or *setweights ()* .

**语法:**

```
dispose()
```

**参数:**

此方法没有参数。

**返回值:**返回*处理结果*。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding a layer
model.add(tf.layers.dense({units: 1, inputShape: [3]}));

// Calling dispose method
const val = model.layers[0].dispose();

// Printing output
console.log(val);
```

**输出:**

```
{
  "refCountAfterDispose": 0,
  "numDisposedVariables": 2
}
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
//import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding layers
model.add(tf.layers.dense({units: 1, inputShape: [5, 1]}));
model.add(tf.layers.dense({units: 4}));
model.add(tf.layers.dense({units: 2, inputShape: [6], batchSize: 5}));

// Calling dispose() method
const val1 = model.layers[0].dispose();
const val2 = model.layers[1].dispose();
const val3 = model.layers[2].dispose();

// Printing output
console.log(val1);
console.log(val2);
console.log(val3);
```

**输出:**

```
{
  "refCountAfterDispose": 0,
  "numDisposedVariables": 2
}
{
  "refCountAfterDispose": 0,
  "numDisposedVariables": 2
}
{
  "refCountAfterDispose": 0,
  "numDisposedVariables": 2
}
```

**参考:**T2【https://js . tensorflow . org/API/latest/# TF . layers . layer . dispose