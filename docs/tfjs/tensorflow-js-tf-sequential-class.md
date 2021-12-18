# Tensorflow.js tf。顺序类

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sequential-class/](https://www.geeksforgeeks.org/tensorflow-js-tf-sequential-class/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

Tensorflow.js **tf。顺序类**是堆叠形式的层集合的模型。这些层连接到各自的相邻层。我们用 tf。顺序()函数创建 tf。顺序类实例。tf。顺序类有许多用于实例的方法。

**语法:**

```
Sequntial_instane.method(args);
```

**参数:**该方法接受以下参数:

*   **args:** 看方法。不同的方法接受不同的参数。

**返回值:**不同的方法返回不同的返回值 *tf。张量*对象等。

**示例 1:** 在本例中，我们将看到 add()方法，该方法用于在图层顶部添加图层。它以图层为参数，返回 void。

## Javascript

```
import * as tf from "@tensorflow/tfjs"

// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs")

async function run() {
    // Creating Instamce 
    const gfg_Instance = tf.sequential();

    // Adding first Layer 
    const Layer1 = tf.layers.dense({ units: 6, inputShape: [2] });
    gfg_Instance.add(Layer1);

    // Adding second layer 
    const layer2 = tf.layers.dense({ units: 3, activation: 'sigmoid' })
    gfg_Instance.add(layer2);

    // Adding third layer
    const layer3 = tf.layers.dense({ units: 2, activation: 'sigmoid' })
    gfg_Instance.add(layer3);

    // Predicting data with layer model.
    const random = tf.randomNormal([4, 2]);
    gfg_Instance.predict(random).print();
}

// Function call
run();
```

**输出:**

```
Tensor
    [[0.5581576, 0.3110509],
     [0.546664 , 0.3369413],
     [0.5634928, 0.2920811],
     [0.5309308, 0.3545613]]
```

**示例 2:** 在本例中，我们将看到 summary()方法，该方法用于打印图层实例的摘要。它采用的是行长度，即摘要的自定义长度，位置是摘要列的宽度，最后是打印功能，用于自定义摘要的输出。它返回空。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs")

async function run() {
    // Creating Instamce 
    const gfg_Instance = tf.sequential();

    // Adding first Layer 
    const Layer1 = tf.layers.dense({ units: 6, inputShape: [2] });
    gfg_Instance.add(Layer1);

    // Adding second layer 
    const layer2 = tf.layers.dense({ units: 3, activation: 'sigmoid' })
    gfg_Instance.add(layer2);

    // Adding third layer
    const layer3 = tf.layers.dense({ units: 2, activation: 'sigmoid' })
    gfg_Instance.add(layer3);

    // Printing summary of layer model 
    gfg_Instance.summary();
}

// Function call
run();
```

**输出:**

```
_________________________________________________________________
Layer (type)                 Output shape              Param #   
=================================================================
dense_Dense34 (Dense)        [null,6]                  18        
_________________________________________________________________
dense_Dense35 (Dense)        [null,3]                  21        
_________________________________________________________________
dense_Dense36 (Dense)        [null,2]                  8         
=================================================================
Total params: 47
Trainable params: 47
Non-trainable params: 0
_________________________________________________________________
```

**参考:**T2】https://js.tensorflow.org/api/latest/#class:Sequential