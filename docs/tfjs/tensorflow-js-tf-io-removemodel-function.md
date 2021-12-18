# tensorlow . js TF . io . remove model()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-io-remove model-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-io-removemodel-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。removeModel()函数**用于通过从记录的存储库介质中提供的网址删除指定的模型。

**语法:**

```
tf.io.removeModel(url)
```

**参数:**

*   **url:** 它是录制的模型中声明的 *URL* ，以及模式前缀，即“localstorage://my-mode-2”、“indexeddb://my/mode/3”。它属于字符串类型。

**返回值:**返回*模型 ArtifactsInfo* 的承诺。

**示例 1:** 使用“logSigmoid”作为激活，“本地存储”作为存储介质。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating model
const mymodel = tf.sequential();

// Calling add() method
mymodel.add(tf.layers.dense(
     {units: 3, inputShape: [20], stimulation: 'logSigmoid'}));

// Calling save() method with a storage medium
await mymodel.save('localstorage://display/command/mymodel1');

// Calling removeModel() method
await tf.io.removeModel('localstorage://display/command/mymodel1');

// Calling listModels() method and
// Printing output
console.log(await tf.io.listModels());
```

**输出:**

```
{
  "localstorage://demo/manage/model1": {
    "dateSaved": "2021-06-24T11:53:05.626Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 613,
    "weightSpecsBytes": 126,
    "weightDataBytes": 44
  },
  "localstorage://demo/managemen/model1": {
    "dateSaved": "2021-06-24T11:52:29.368Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 611,
    "weightSpecsBytes": 124,
    "weightDataBytes": 44
  },
  "localstorage://demo/management/model2": {
    "dateSaved": "2021-06-24T11:53:33.384Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 613,
    "weightSpecsBytes": 126,
    "weightDataBytes": 44
  },
  "localstorage://demo/management/model": {
    "dateSaved": "2021-06-24T11:53:26.006Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 613,
    "weightSpecsBytes": 126,
    "weightDataBytes": 44
  },
  "localstorage://display/command/mymodel2": {
    "dateSaved": "2021-06-24T19:02:03.367Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 612,
    "weightSpecsBytes": 125,
    "weightDataBytes": 32
  },
  "indexeddb://demo/management/model1": {
    "dateSaved": "2021-06-24T13:02:20.265Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 614,
    "weightSpecsBytes": 126,
    "weightDataBytes": 44
  },
  "indexeddb://display/command/mymodel": {
    "dateSaved": "2021-06-24T18:50:50.602Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 613,
    "weightSpecsBytes": 126,
    "weightDataBytes": 252
  },
  "indexeddb://display/command/mymodel1": {
    "dateSaved": "2021-06-24T18:59:17.435Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 612,
    "weightSpecsBytes": 125,
    "weightDataBytes": 32
  },
  "indexeddb://example/command/mymodel": {
    "dateSaved": "2021-06-24T12:33:06.208Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 613,
    "weightSpecsBytes": 126,
    "weightDataBytes": 1428
  }
}
```

**示例 2:** 使用“prelu”作为激活，“IndexedDB”作为存储介质，使用“JSON.stringify”以字符串格式返回输出。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating model
const mymodel = tf.sequential();

// Calling add() method
mymodel.add(tf.layers.dense(
     {units: 11, inputShape: [6], stimulation: 'prelu'}));

// Calling save() method with a storage medium
await mymodel.save('indexeddb://display/command/mymodel1');

// Calling removeModel() method
await tf.io.removeModel('indexeddb://display/command/mymodel1');

// Calling listModels() method and
// Printing output
console.log(JSON.stringify(await tf.io.listModels()));
```

**输出:**

```
{
  "localstorage://demo/manage/model1": {
    "dateSaved": "2021-06-24T11:53:05.626Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 613,
    "weightSpecsBytes": 126,
    "weightDataBytes": 44
  },
  "localstorage://demo/managemen/model1": {
    "dateSaved": "2021-06-24T11:52:29.368Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 611,
    "weightSpecsBytes": 124,
    "weightDataBytes": 44
  },
  "localstorage://demo/management/model2": {
    "dateSaved": "2021-06-24T11:53:33.384Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 613,
    "weightSpecsBytes": 126,
    "weightDataBytes": 44
  },
  "localstorage://demo/management/model": {
    "dateSaved": "2021-06-24T11:53:26.006Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 613,
    "weightSpecsBytes": 126,
    "weightDataBytes": 44
  },
  "localstorage://display/command/mymodel2": {
    "dateSaved": "2021-06-24T19:02:03.367Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 612,
    "weightSpecsBytes": 125,
    "weightDataBytes": 32
  },
  "indexeddb://demo/management/model1": {
    "dateSaved": "2021-06-24T13:02:20.265Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 614,
    "weightSpecsBytes": 126,
    "weightDataBytes": 44
  },
  "indexeddb://display/command/mymodel": {
    "dateSaved": "2021-06-24T18:50:50.602Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 613,
    "weightSpecsBytes": 126,
    "weightDataBytes": 252
  },
  "indexeddb://example/command/mymodel": {
    "dateSaved": "2021-06-24T12:33:06.208Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 613,
    "weightSpecsBytes": 126,
    "weightDataBytes": 1428
  }
}

```

**参考:**T2】https://js.tensorflow.org/api/latest/#io.removeModel