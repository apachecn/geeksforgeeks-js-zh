# Tensorflow.js tf.io.http()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-io-http-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-io-http-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**.io.http()函数**用于生成 *IOHandler* 子集，该子集将模型工件传输到 http 服务器。此外，<sub>多部分</sub>或<sub>表单数据</sub> mime 类型的 HTTP 请求将被传输到*路径*网址。其中，表单数据包含描述模型拓扑和/或模型权重的工件。

**语法:**

```
tf.io.http(path, loadOptions?)
```

**参数:**

*   **路径:**模型的指定网址路径。此外，它可以是完整的 HTTP 路径，即“HTTP://localhost:8000/model-upload”或类似的路径，即。/model-upload '。它属于字符串类型。
*   **装载选项:**装载目的的规定配置。它是可选的，类型为*装载选项*。它包括以下字段:
    1.  **权重路径前缀:**权重文件路径的指定可选前缀。此外，默认情况下，此的值是从路径参数中计算的。
    2.  **提取功能:**所述的可选自定义<sub>提取</sub>功能。
    3.  **onProgress:** 所述的可选进度回调功能，在加载完成前定期释放。

**返回值:**返回 *IOHandler* 。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling io.http() method
const result = tf.io.http('https://js.tensorflow.org/api/latest/#io.http');

// Printing output
console.log(result);
```

**输出:**

```
{
  "DEFAULT_METHOD": "POST",
  "path": "https://js.tensorflow.org/api/latest/#io.http",
  "requestInit": {}
}
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating model
const model = tf.sequential();

// Adding layer to the model
model.add(
     tf.layers.dense({units: 2, inputShape: [10]}));

// Calling io.http() method within 
// save() method
const result = await model.save(tf.io.http(
     'https://js.tensorflow.org/api/latest/#io.http'));

// Printing output
console.log(result);
```

**输出:**

```
{
  "modelArtifactsInfo": {
    "dateSaved": "2021-08-26T08:43:49.648Z",
    "modelTopologyType": "JSON",
    "modelTopologyBytes": 611,
    "weightSpecsBytes": 124,
    "weightDataBytes": 88
  },
  "responses": [
    {}
  ]
}
```

**参考:**T2】https://js.tensorflow.org/api/latest/#io.http