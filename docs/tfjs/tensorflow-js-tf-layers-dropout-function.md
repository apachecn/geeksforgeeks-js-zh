# tensorflow . js TF . layers . drop()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-drop-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-dropout-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**TF . layers . drop()**函数是 **Tensorflow.js** 库的内置函数。该函数用于防止模型中的过拟合，方法是在训练期间每次更新时，随机将输入单位的分数设置为 0。

**语法:**

```
tf.layers.dropout( {rate} )
```

**参数:**

*   **参数:**给定对象作为参数。
*   **速率:**指定要下降的输入单位的分数。它的值介于 0 和 1 之间。
*   **噪声形状:**整数列表，表示将与输入相乘的缺失形状。这是一个可选参数。
*   **种子:**指定随机种子。这是一个可选参数。
*   **输入形状:**如果定义了该参数，它将创建另一个输入层插入到该层之前。
*   **batchInputShape:** 如果定义了这个参数，它会创建另一个输入图层，插入到这个图层之前。
*   **batchSize:** 用于构造 batchInputShape，如果尚未指定。
*   **数据类型:**指定该图层的数据类型。此参数的默认值为“float32”。
*   **名称:**指定该图层的名称。
*   **可训练:**指定是否通过拟合更新该层的权重。
*   **权重:**指定图层的初始权重值。
*   **输入类型:**用于表示输入类型，其值可以是“float32”或“int32”或“bool”或“complex64”或“string”。

**返回值:**返回压差。

**示例 1:** 我们将创建一个新模型，并在其中添加脱落层。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs");

// Define the model
const model = tf.sequential({
    layers: [tf.layers.dense({ 
        units: 1, inputShape: [10] 
    })],
});

// Add dropout to model
model.add(tf.layers.dropout({ rate: 0.25 }));

// Compile the model
model.compile(
    { optimizer: "sgd", loss: "meanAbsoluteError" },
    (metrics = ["accuracy"])
);

// Evaluate the model
const result = model.evaluate(
    tf.ones([8, 10]), tf.ones([8, 1]), {
    batchSize: 4,
});

// Print the resulting tensor
result.print();
```

**输出:**

```
Tensor
    1.608272910118103
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs");

// Define the model
const model = tf.sequential({
    layers: [tf.layers.dense({ 
        units: 1, inputShape: [10] 
    })],
});

// Add dropout to model
model.add(tf.layers.dropout({ rate: 0.5 }));

// Compile the model
model.compile({ optimizer: "adam", 
    loss: "meanSquaredError" });

// Evaluate the model
const result = model.evaluate(
    tf.ones([8, 10]), tf.ones([8, 1]), {
    batchSize: 2,
});

// Print the result
result.print();
```

**输出:**

```
Tensor
    0.9941154718399048
```

**参考:**T2】https://js.tensorflow.org/api/latest/#layers.dropout