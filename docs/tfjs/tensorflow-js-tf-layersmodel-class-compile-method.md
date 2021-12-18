# Tensorflow.js tf。LayersModel 类。编译()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers model-class-compile-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layersmodel-class-compile-method/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**。compile()** 功能配置并制作用于训练和评估过程的模型。通过打电话。compile()函数我们准备了带有优化器、损失和度量的模型。那个。compile()函数将参数对象作为参数。

**注:**如果你叫**。飞度()**或**。在未编译的模型上求值()**函数，那么程序会抛出一个错误。

**语法:**

```
tf.model.compile({optimizer, loss}, metrics=[])
```

**参数:**

*   **Optimizer:** It is a mandatory parameter. It accepts the object of tf.train.Optimizer or the string name of Optimizer. The following is the string name of the optimizer- **[SGD]** **[Adam]** **[Adamax]** **[Adadelta]** **[Adagrad]** **[RMSProp] [T11**
*   **Loss:** is a required parameter. It accepts a string value or string array as the loss type. If our model has multiple outputs, we can use different losses on each output by passing an array of losses. The loss value that the model will minimize will be the sum of all individual losses. The following are the names of the lost strings-T2, mean square error, T3, T4, mean absolute error, T5, etc.
*   **Measurement:** is an optional parameter. It accepts the list of indicators evaluated by the model in the training and testing stages. Normally, we use ***to measure = ['accuracy']*** In order to specify different metrics for different outputs of the multi-output model, we can also pass a dictionary.

**返回值:**由于是为训练准备模型，所以不返回任何东西。(即返回类型无效)

**示例 1:** 在本例中，我们将创建一个简单的模型，并传递**优化器**和**损耗**参数的值。这里我们使用**优化器**作为**“Adam”**，**损失**作为**“mean squared error”**。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs");

// define the model
const model = tf.sequential({
    layers: [tf.layers.dense({ units: 1, inputShape: [10] })],
});

// compile the model
// using "adam" optimizer and "meanSquaredError" loss
model.compile({ optimizer: "adam", loss: "meanSquaredError" });

// evaluate the model which was compiled above
// computation is done in batches of size 4
const result = model.evaluate(tf.ones([8, 10]), tf.ones([8, 1]), {
    batchSize: 4,
});

// print the result
result.print();
```

**输出:**

```
Tensor
    2.6806342601776123
```

**示例 2:** 在本例中，我们将创建一个简单的模型，并传递**优化器**、**损耗**和度量参数的值。这里我们使用优化器作为**【SGD】**，使用损失作为**【意味着绝对错误】**和**【准确性】**作为度量。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs");

// define the model
const model = tf.sequential({
    layers: [tf.layers.dense({ units: 1, inputShape: [10] })],
});

// compile the model
// using "adam" optimizer, "meanSquaredError" loss and "accuracy" metrics
model.compile(
    { optimizer: "adam", loss: "meanSquaredError" },
    (metrics = ["accuracy"])
);

// evaluate the model which was compiled above
// computation is done in batches of size 4
const result = model.evaluate(tf.ones([8, 10]), tf.ones([8, 1]), {
    batchSize: 4,
});

// print the result
result.print();
```

**输出:**

```
Tensor
    1.4847172498703003
```

**示例 3:** 在本例中，我们将创建一个简单的模型，并传递**优化器**、**损耗**和**度量**参数的值。这里我们使用优化器作为**【SGD】**，使用损失作为**【意味着绝对误差】**和**【精度】**作为度量。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs");

// define the model
const model = tf.sequential({
    layers: [tf.layers.dense({ units: 1, inputShape: [10] })],
});

// compile the model
// using "adam" optimizer, "meanSquaredError" loss and "accuracy" metrics
model.compile(
    { optimizer: "sgd", loss: "meanAbsoluteError" },
    (metrics = ["precision"])
);

// evaluate the model which was compiled above
// computation is done in batches of size 4
const result = model.evaluate(tf.ones([8, 10]), tf.ones([8, 1]), {
    batchSize: 4,
});

// print the result
result.print();
```

**输出:**

```
Tensor
   1.507279634475708
```

**参考:**[https://js.tensorflow.org/api/latest/#tf.layer model . compile](https://js.tensorflow.org/api/latest/#tf.LayersModel.compile)