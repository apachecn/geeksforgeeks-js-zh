# Tensorflow.js tf。GraphModel 类。保存()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-graph model-class-save-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-graphmodel-class-save-method/)

**简介:** Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型以及深度学习神经网络。

**。保存()功能**用于保存所述*图形模型*的结构和/或重量。

**注:**

*   An *iohandler* is an object, which has a saving method about the specified exact signature.
*   *The method of saving* controls the accumulation or transmission of sequential data, that is, artifacts describing the model topology and the weights on or through a specific medium, such as *local storage file* , *file download* , *index database* and HTTP request to the server in the web browser.
*   tensor low . jsaā0〔t1〕iohandler〔t1〕是 Tao，āNSO(t1)是 Tao . io。浏览器下载()*TF。我，我。浏览器本地存储*。
*   In addition, this method also allows us to apply specific kinds of *iohandlers* , such as URL-like string technology, such as *"local storage://"and "indexed db://"*.

**语法:**

```
save(handlerOrURL, config?)
```

**参数:**

*   **handle URL: the instance of *iohandler* described in** , or the URL based on the design string technology similar to *iohandler* . It is *IO type. IOHandler|string* 。
*   **Configure:** The option is used to save the model. It is optional and belongs to the object type. It has two parameters as follows:

1.  **Trainable only:** It states that if only the trainable weight of the model is saved, the untrained weight will be ignored. Type *Boolean* , which is false by default.
2.  [T0】 include optimizer: 【T1] indicates whether to store the optimizer. Type *Boolean* , which is false by default.

**返回值:**返回 io.SaveResult 的承诺。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining model url
const model_Url =
'https://storage.googleapis.com/tfjs-models/savedmodel/mobilenet_v2_1.0_224/model.json';

// Calling the loadGraphModel() method
const mymodel = await tf.loadGraphModel(model_Url);

// Calling save() method
const output = await mymodel.save('downloads://mymodel');

// Printing output
console.log(output)
```

**输出:**

```
{
  "modelArtifactsInfo": {
    "dateSaved": "2021-08-19T12:00:15.603Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 90375,
    "weightSpecsBytes": 15791,
    "weightDataBytes": 13984940
  }
}
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling the loadGraphModel() method
const mymodel = await tf.loadGraphModel(
'https://storage.googleapis.com/tfjs-models/savedmodel/mobilenet_v2_1.0_224/model.json');

// Calling save() method with all its
// parameters
const output = await mymodel.save('downloads://mymodel', true, true);

// Printing output
console.log(JSON.stringify(output))
```

**输出:**

```
{"modelArtifactsInfo":{"dateSaved":"2021-08-19T12:05:35.906Z",
"modelTopologyType":"JSON","modelTopologyBytes":90375,
"weightSpecsBytes":15791,"weightDataBytes":13984940}}
```

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.GraphModel.save