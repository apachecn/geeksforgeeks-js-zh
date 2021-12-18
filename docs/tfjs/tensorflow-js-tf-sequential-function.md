# tensorflow . js . TF . sequential()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sequential-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-sequential-function/)

当你想创建一个没有多重输入和输出的模型，并且它将被一层一层地开发时，那么我们将选择深度学习的顺序模型。基本上有两种类型的模型功能和顺序模型。因此在本文中，我们将在 Tensorflow.js 中看到带有 tf.sequential()的 Sequential 模型

tf.sequential()函数创建了一个模型，其中一层的一个输出是下一层的输入。简单来说，我们可以说它是一个没有分支和跳过的线性层叠。

**语法:**

```
tf.sequential( layers, name )
```

**参数:**

*   **图层:**是我们要添加到模型中的图层列表。
*   **名称:**车型名称。

**示例 1:** 在本例中，我们将创建一个具有 2 个输入形状 3 的密集层的序列模型，并使用该模型进行一些预测。

在 inputShape 中:[null，3]第一个参数是未确定的批处理维度，第二个参数是模型最后一层的输出大小。您可以通过输入形状:[空，3]或输入形状:[3]

## Javascript

```
// Import Tensorflow.js
import * as tf from "@tensorflow/tfjs"

// Create model tf.sequential() method
// Here you need to specify the input 
// shape for first layer manually and
// for the second layer it will 
// automatilly update
var model = tf.sequential({ 
    layers: [tf.layers.dense({units:1,inputShape:[3]}),
    tf.layers.dense({units:4})] 
});

// Prediction with model
console.log('Lets Predict Something:');
model.predict(tf.ones([1,3])).print();
```

**输出:**

```
Lets Predict Something:
Tensor
    [[-1.1379941, 0.945751, -0.1970642, -0.5935861],]
```

**示例 2:** 在本例中，我们将使用 model.add()函数向模型中添加一个密集层，从而创建一个具有 2 个密集层的输入形状 16 的模型。

## Javascript

```
// Import Tensorflow.js
import * as tf from "@tensorflow/tfjs"

// Create sequantial model
var model = tf.sequential();

// Add dense layer using model.add() 
model.add(tf.layers.dense({units:8, inputShape: [16]}));

model.add(tf.layers.dense({units:4}));

// Predict something
console.log('Lets predict something:');
model.predict(tf.ones([8,16])).print();
```

```
Output :
Lets predict something:
Tensor
   [[0.9305074, -0.7196146, 0.5809593, -0.08824],
    [0.9305074, -0.7196146, 0.5809593, -0.08824],
    [0.9305074, -0.7196146, 0.5809593, -0.08824],
    [0.9305074, -0.7196146, 0.5809593, -0.08824],
    [0.9305074, -0.7196146, 0.5809593, -0.08824],
    [0.9305074, -0.7196146, 0.5809593, -0.08824],
    [0.9305074, -0.7196146, 0.5809593, -0.08824],
    [0.9305074, -0.7196146, 0.5809593, -0.08824]]
```

**参考文献:**T2】https://js.tensorflow.org/api/latest/#sequential