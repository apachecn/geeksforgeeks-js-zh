# Tensorflow.js tf。GraphModel 类。预测()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-graph model-class-predict-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-graphmodel-class-predict-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。predict()函数**用于实现有利于输入张量的蕴涵。

**语法:**

```
predict(inputs, config?)
```

**参数:**

*   **输入:**是规定的输入。它属于类型(tf。张量|tf。Tensor[]|{[name: string]: tf。Tensor})。
*   **配置:**这是规定的预测配置，用于定义批次大小以及输出节点名称。此外，目前图形模型忽略了批量选择。它是可选的，属于对象类型。
    *   **批次尺寸:**是所述批次尺寸，可选，类型为整数。如果未定义，那么缺省值将是 32。
    *   **详细:**这是规定的详细模式，其默认值为假，是可选的。

**返回值:**返回 tf。张量|tf。Tensor[]|{[name: string]: tf。张量}。

**示例 1:** 在本例中，我们从一个 URL 加载 MobileNetV2，并保存一个带有零输入的预测。

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

// Calling predict() method and 
// Printing output
mymodel.predict(inputs).print();
```

**输出:**

```
Tensor
     [[-0.1800361, -0.4059965, 0.8190175, 
     ..., 
     -0.8953396, -1.0841646, 1.2912753],]
```

**示例 2:** 在本例中，我们从 TF Hub URL 加载 MobileNetV2，并保存一个带有零输入的预测。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const model_Url =
'https://tfhub.dev/google/imagenet/mobilenet_v2_140_224/classification/2';

// Calling the loadGraphModel() method
const model = await tf.loadGraphModel(
        model_Url, {fromTFHub: true});

// Defining inputs
const inputs = tf.zeros([1, 224, 224, 3]);

// Defining batchsize
const batchsize = 1;

// Defining verbose
const verbose = true;

// Calling predict() method and
// Printing output
model.predict(inputs, batchsize, verbose).print();
```

**输出:**

```
Tensor
     [[-1.1690605, 0.0195426, 1.1962479, 
     ..., 
     -0.4825858, -0.0055641, 1.1937635],]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.GraphModel.predict