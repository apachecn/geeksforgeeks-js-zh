# Tensorflow.js tf。顺序类。总结()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sequential-class-summary-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-sequential-class-summary-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。tensorflow.js 中的 summary()函数**用于打印有利于顺序模型的图层的文本摘要。此外，它包括包括模型的每个层的名称和类型、层的输出配置、每个层的权重参数计数、所述模型的可训练和不可训练参数的绝对计数。

**语法:**

```
summary(lineLength?, positions?, printFn?)
```

**参数:**

*   **行长:**是字符列表中规定的自定义行长。它是可选的，并且是数字类型。
*   **位置:**是所有列的自定义大小，如*行长度的分数*即*【0.25，0.5，0.75】或字符的绝对列表即【20，40，55】。这里，每个数字都属于所述列的结束位置，即右侧位置。它是可选的，类型为数字[]。*
*   ***打印 Fn:** 是指定的自定义打印功能，用来替代默认值*控制台. log* 。它是可选参数。*

***返回值:**返回 void。*

***例 1:** 调用没有任何参数的 summary()方法。*

## *Javascript*

```
*// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining model
const myModel = tf.sequential();

// Calling add() method to add layers
myModel.add(
     tf.layers.dense({units: 4, inputShape: [20], initiation: 'prelu'}));
myModel.add(tf.layers.dense({units:2 , initiation: 'logSigmoid'}));

// Calling summary method and 
// Printing output
myModel.summary();*
```

***输出:***

```
*_________________________________________________________________
Layer (type)                 Output shape              Param #   
=================================================================
dense_Dense121 (Dense)       [null,4]                  84        
_________________________________________________________________
dense_Dense122 (Dense)       [null,2]                  10        
=================================================================
Total params: 94
Trainable params: 94
Non-trainable params: 0
_________________________________________________________________*
```

***例 2:** 用参数调用 summary()方法。*

## *Javascript*

```
*// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling summary method with its
// parameters and printing output
 tf.sequential({ 
    layers:[tf.layers.dense({units: 7, inputShape: [6]})]
 }).summary({lineLength: 4}, {positiions: [1, 2, 4]});*
```

***输出:***

```
*Layer (type Output shap Param #

dense_Dense189 (Dense [null,7 49

Total params: 49
Trainable params: 49
Non-trainable params: 0*
```

***参考:**T2】https://js.tensorflow.org/api/latest/#tf.Sequential.summary*