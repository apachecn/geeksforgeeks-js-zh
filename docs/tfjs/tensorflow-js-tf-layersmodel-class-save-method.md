# Tensorflow.js tf。LayersModel 类。保存()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers model-class-save-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layersmodel-class-save-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。保存()功能**用于保存所述*图层模型*的结构和/或重量。

**注意:**

*   IOHandler is an object that has a saving method about the specified exact signature.
*   Save method controls the accumulation or transmission of sequential data, that is, the artifacts describing the model topology and the weights on or through specific media, such as local storage files, file downloads, index databases in web browsers and HTTP requests to servers.
*   tensorflow 管理员、浏览器下载()TF . io . browserlocalstorage。
*   In addition, this method also allows us to apply specific types of IOHandler, such as URL-like string technologies, such as "localstorage://" and "indexeddb://".

**语法:**

```
save(handlerOrURL, config?)
```

**参数:**

*   **handle URL:** the declared instance of IOHandler, or a URL similar to the string technology based on design that supports iohandler. It is of io type. IOHandler | string.
*   **Configure:** the option to save the model number. It is optional and belongs to the object type. It has two parameters as follows:
    1.  **Trainable only:** It states whether to save only the trainable weight of the model and ignore the untrained weight. It belongs to Boolean type, and the default value is false.
    2.  [T0】 include optimizer: 【T1] indicates whether to store the optimizer. It belongs to Boolean type, and the default value is false.

**返回值:**返回 io.SaveResult 的承诺。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential(
     {layers: [tf.layers.dense({units: 2, inputShape: [2]})]});

// Calling save() method
const res = await model.save('localstorage://mymodel');

// Printing output
console.log(res)
```

**输出:**

```
{
  "modelArtifactsInfo": {
    "dateSaved": "2021-08-23T09:53:28.198Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 612,
    "weightSpecsBytes": 125,
    "weightDataBytes": 24
  }
}
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential(
     {layers: [tf.layers.dense({units: 2, inputShape: [2]})]});

// Calling save() method
const res = await model.save('localstorage://mymodel', true, true);

// Printing output
console.log(JSON.stringify(res))
```

**输出:**

```
{"modelArtifactsInfo":{"dateSaved":"2021-08-23T09:55:33.044Z",
"modelTopologyType":"JSON","modelTopologyBytes":612,
"weightSpecsBytes":125,"weightDataBytes":24}}
```

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.LayersModel.save