# Tensorflow.js tf。LayersModel 类。总结()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers model-class-summary-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layersmodel-class-summary-method/)

tf。layer model 是 tensorflow.js 中用于训练、推断和评估层模型的类。它包含用于训练、评估、预测和保存层模型的方法。所以在这篇文章中，我们将了解 model.summary()函数。

tensorflow.js 中的 **model.summary()** 函数打印模型的摘要，它包括模型的名称、权重参数的数量、可训练参数的数量。

**语法:**

```
model_name.summary (line length, position, print function)
```

**参数:**所有参数可选。

*   **行长:**是一个自定义的行长，以若干字符为单位。
*   **位置:**是一个显示每列宽度的数组，值可以是小数也可以是绝对值。
*   **打印功能:**打印车型汇总的功能，默认功能为 console.log()。

**返回:**作废。

**示例 1:** 在本例中，我们将创建具有单个密集层的序列模型，并使用 model.summary()函数打印模型的摘要。

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Creating model
var myModel = tf.sequential({
    layers:[tf.layers.dense({
        units: 10,
        inputShape: [15]
    })]
});

// Print the summary
myModel.summary();
```

**输出:**

```
_________________________________________________________________
Layer (type)                 Output shape              Param #    
=================================================================
dense_Dense8 (Dense)         [null,10]                 160        
=================================================================
Total params: 160
Trainable params: 160
Non-trainable params: 0
_________________________________________________________________
```

**示例 2:** 在此示例中，我们将使用 tf.model 方法创建具有 2 个密集层的模型，这 2 个密集层具有激活函数 relu 和 softmax，并进行预测，同时打印模型的摘要。

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Define input
var inp=tf.input({shape:[8]});

// Dense layer 1
var denseLayerOne=tf.layers.dense({units:7,activation:'relu'});

// Dense layer 1
var denseLayerTwo=tf.layers.dense({units:5, activation:'softmax'});

// Generate the output
var out=denseLayerTwo.apply(denseLayerOne.apply(inp));

// Model creation
var myModel=tf.model({inputs:inp,outputs:out});

// Make prediction
console.log("\nPrediction :")
myModel.predict(tf.ones([3,8])).print();
console.log("\nSummary :")
myModel.summary();
```

**输出:**

```
Prediction :
Tensor
   [[0.2074656, 0.1515629, 0.2641615, 0.2237201, 0.1530899],
    [0.2074656, 0.1515629, 0.2641615, 0.2237201, 0.1530899],
    [0.2074656, 0.1515629, 0.2641615, 0.2237201, 0.1530899]]

Summary :
_________________________________________________________________
Layer (type)                 Output shape              Param #    
=================================================================
input7 (InputLayer)          [null,8]                  0          
_________________________________________________________________
dense_Dense19 (Dense)        [null,7]                  63        
_________________________________________________________________
dense_Dense20 (Dense)        [null,5]                  40        
=================================================================
Total params: 103
Trainable params: 103
Non-trainable params: 0
_________________________________________________________________
```

**参考:**[https://js.tensorflow.org/api/latest/#tf.layer model . summary](https://js.tensorflow.org/api/latest/#tf.LayersModel.summary)