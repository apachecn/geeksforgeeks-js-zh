# tensorflow . js . TF . layers addLoss()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-add loss-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-addloss-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。addLoss()功能**用于将损耗附加到所述层。此外，损耗可能取决于一些输入张量，例如，操作损耗取决于所述层的输入。

**语法:**

```
addLoss(losses)
```

**参数:**

*   **损失:**是所述损失。可以是*正则化*或*正则化*类型。

**返回值:**返回 void。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding a layer
model.add(tf.layers.dense({units: 1, inputShape: [3]}));

// Defining input
const input = tf.tensor1d([1, 2, 3, 4]);

// Calling addLoss() method with its 
// parameter
const res = model.layers[0].addLoss([tf.abs(input)]);

// Printing output
console.log(JSON.stringify(input));
model.layers[0].getWeights()[0].print();
```

**输出:**

```
{"kept":false,"isDisposedInternal":false,"shape":[4],"dtype":"float32",
"size":4,"strides":[],"dataId":{"id":82},"id":124,"rankType":"1","scopeId":61}
Tensor
    [[0.143441  ],
     [-0.58002  ],
     [-0.5836995]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding layers
model.add(tf.layers.dense({units: 1, inputShape: [3]}));
model.add(tf.layers.dense({units: 4}));
model.add(tf.layers.dense({units: 9, inputShape: [11]}));

// Defining inputs
const input1 = tf.tensor1d([0.5, 0.2, -33, null]);
const input2 = tf.tensor1d([0.33, 0.5, -1]);
const input3 = tf.tensor1d([1, 0.44]);

// Calling addLoss() method with its 
// parameter
const res1 = model.layers[0].addLoss([tf.cos(input1)]);
const res2 = model.layers[0].addLoss([tf.sin(input2)]);
const res3 = model.layers[0].addLoss([tf.tan(input3)]);

// Printing outputs
console.log(JSON.stringify(input1));
console.log(JSON.stringify(input2));
console.log(JSON.stringify(input3));
model.layers[0].getWeights()[0].print();
```

**输出:**

```
 {"kept":false,"isDisposedInternal":false,"shape":[4],"dtype":"float32",
 "size":4,"strides":[],"dataId":{"id":169},"id":261,"rankType":"1","scopeId":112}
{"kept":false,"isDisposedInternal":false,"shape":[3],"dtype":"float32",
"size":3,"strides":[],"dataId":{"id":170},"id":262,"rankType":"1","scopeId":112}
{"kept":false,"isDisposedInternal":false,"shape":[2],"dtype":"float32",
"size":2,"strides":[],"dataId":{"id":171},"id":263,"rankType":"1","scopeId":112}
Tensor
    [[-0.0062826],
     [0.0883235 ],
     [-1.0633234]]
```

**参考:**[https://js . tensorflow . org/API/latest/# TF . layers . layer . addloss](https://js.tensorflow.org/api/latest/#tf.layers.Layer.addLoss)