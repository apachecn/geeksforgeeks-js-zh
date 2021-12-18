# Tensorflow.js tf。GraphModel 类。处置()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-graph model-class-dispose-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-graphmodel-class-dispose-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。dispose()函数**用于释放权重张量和 resourceManager 正在使用的内存。

**语法:**

```
dispose()
```

**参数:**

此方法不包含任何参数。

**返回值:**返回 void。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const model_Url =
'https://storage.googleapis.com/tfjs-models/savedmodel/mobilenet_v2_1.0_224/model.json';

// Calling the loadGraphModel() method
const mymodel = await tf.loadGraphModel(model_Url);

// Calling dispose() method
mymodel.dispose();

// Printing output
console.log('Model Disposed.');
```

**输出:**

```
Model Disposed.
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const model_Url =
'https://storage.googleapis.com/tfjs-models/savedmodel/mobilenet_v2_1.0_224/model.json';

// Calling the loadGraphModel() method
const mymodel = await tf.loadGraphModel(model_Url);

// Defining inputs
const inputs = tf.zeros([1, 224, 224, 3]);

// Calling dispose() method
mymodel.dispose();

// Calling execute() method and
// Printing output
mymodel.execute(inputs).print();
```

**输出:**

```
An error occured
Cannot read property 'backend' of undefined
```

在这里，出现了一个错误，并且输出没有被打印，因为所述模型已经被处理。因此，execute()方法不能返回任何输出。

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.GraphModel.dispose