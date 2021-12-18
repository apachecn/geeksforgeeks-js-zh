# tensorflow . js TF . io . move model()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-io-move model-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-io-movemodel-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。moveModel()函数**用于将一个模型从一个网址移动到一个新的网址。此外，这种方法有利于在存储介质内部(即在同一种记录介质内)或在两种存储介质之间(即在不同种记录介质之间)的移动。

**语法:**

```
tf.io.moveModel(sourceURL, destURL)
```

**参数:**

*   **源 URL:** 是规定的移动源 URL。它属于字符串类型。
*   **destURL:** 是所述的移动目的地 URL。它属于字符串类型。

**返回值:**返回*模型 ArtifactsInfo* 的承诺。

**示例 1:**

*   Movement between two different storage media.
*   Use "logSigmoid" as activation, "local storage" and "IndexedDB" as storage media.

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
await mymodel.save('localstorage://display/command/mymodel');

// Calling moveModel() method with its parameters
await tf.io.moveModel(
     'localstorage://display/command/mymodel',
     'indexeddb://display/command/mymodel1');

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
  "localstorage://demo/managemen/model1": {
    "dateSaved": "2021-06-24T11:52:29.368Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 611,
    "weightSpecsBytes": 124,
    "weightDataBytes": 44
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
    "dateSaved": "2021-06-24T18:55:00.803Z",
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

**例 2:**

*   Internal movement of similar storage media.
*   Use "prelu" as the activation, "Local Storage" as the storage medium and "JSON.stringify" to return the output in string format.

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating model
const mymodel = tf.sequential();

// Calling add() method
mymodel.add(tf.layers.dense(
     {units: 1, inputShape: [7], stimulation: 'prelu'}));

// Calling save() method with a storage medium
await mymodel.save('localstorage://display/command/mymodel1');

// Calling moveModel() method with its parameters
await tf.io.moveModel(
     'localstorage://display/command/mymodel1',
     'localstorage://display/command/mymodel2');

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

**参考:**T2】https://js.tensorflow.org/api/latest/#io.moveModel