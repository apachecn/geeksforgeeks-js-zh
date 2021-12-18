# tensorflow . js TF . layers . activation()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-activation-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-activation-function/)

**简介:** Tensorflow.js 是 Google 开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。tensorflow . js TF . layers . activation()函数用于将函数应用于我们输入层的所有元素。我们还可以将函数应用于具有密集层的输入数据。

**语法:**

```
tf.layers.activation(args);    
```

**参数:**以下是该函数接受的参数:

*   **Parameter:** is an object type with fields:
    *   **Activation:** is the name of the function applied to all input elements.
    *   **Input shape:** is the shape of the input layer of the model. It is used to create the input layer.
    *   [T0】 batchInputShape: 【T1] used to make the input layer. It defines the shape of the batch for the samples in the input layer.
    *   **Batch size:** Used to make the input layer. It is the complement of batchInputShape in the input layer structure.
    *   **Data type:** defines the data type of the layer. It is used for the first layer of the model.
    *   **Name:** It declares a string, that is, the name of the input layer.
    *   **Trainable:** Declare whether a layer can be trained or not through a function. It is a Boolean data type.
    *   **Weight:** is a tensor and the initial data of a layer.
    *   [T0】 input type: 【T1] is the data type of the input data in the layer.

**返回:**激活

下面是这个函数的一些例子:

**示例 1:** 在本例中，我们将制作激活层并检查返回值。

## Javascript

```
import * as tf from "@tensorflow/tfjs"

// Creatomg config for the activation layer
const config = {
    activation: 'sigmoid',
    inpurShape: 5,
    dtype: 'int32',
    name: 'activationLayer'
};

// Defining the activation layer
const activationLayer = tf.layers.activation(config);

// printing return of activation layer
console.log(activationLayer);
```

**输出:**

```
{
  "_callHook": null,
  "_addedWeightNames": [],
  "_stateful": false,
  "id": 38,
  "activityRegularizer": null,
  "inputSpec": null,
  "supportsMasking": true,
  "_trainableWeights": [],
  "_nonTrainableWeights": [],
  "_losses": [],
  "_updates": [],
  "_built": false,
  "inboundNodes": [],
  "outboundNodes": [],
  "name": "ActivationLayer",
  "trainable_": true,
  "initialWeights": null,
  "_refCount": null,
  "fastWeightInitDuringBuild": false,
  "activation": {}
}
```

**示例 2:** 在本例中，我们将使用一些配置创建我们的激活层，并使用激活层训练我们的输入数据。

## Javascript

```
import * as tf from "@tensorflow/tfjs"

// Configuration file for the activation layer
const geek_config = {
    activation: 'sigmoid',
    inpurShape: 5,
    dtype: 'int32',
    name: 'activationLayer'
};

const geek_activation = tf.layers.activation(geek_config);
const geek_inputLayer = tf.layers.dense({units: 1});

// Our Input layer for the model
const geek_input = tf.input({shape: [7]});

// Making structure for the model
const geek_output = geek_inputLayer.apply(geek_input);
const geek_result = geek_activation.apply(geek_output);

// Making Model from struncture 
const config2 = {inputs: geek_input, outputs: geek_result}
const model = tf.model(config2);

// Collect both outputs and print separately.
const config3 = tf.randomUniform([4, 7])
const  geek_activationResult = model.predict(confg3);
geek_activationResult.print();
```

**输出:**

```
Tensor
    [[0.4178988],
     [0.2027801],
     [0.2813435],
     [0.2546847]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#layers.activation