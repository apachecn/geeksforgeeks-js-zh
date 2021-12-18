# Tensorflow.js tf。LayersModel 类。配合()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers model-class-fit-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layersmodel-class-fit-method/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**tf。LayersModel 类。fit()方法**用于为固定数量的时期(数据集上的迭代)训练模型。

**语法:**

```
fit(x, y, args?)
```

**参数:**该方法接受以下参数。

*   **x:** 是 tf。包含所有输入数据的张量。
*   **y:** 是 tf。包含所有输出数据的张量。
*   **args:** 是对象类型，它的变量如下:
    1.  **batchSize:** 它定义了将通过训练传播的样本数量。
    2.  **时期:**它定义了训练数据数组的迭代。
    3.  **详细:**它有助于显示每个纪元的进度。如果该值为 0–表示在 fit()调用期间没有打印消息。如果值为 1–这意味着在 Node-js 中，它会打印进度条。在浏览器中，它不显示任何操作。值 1 是默认值。2–值 2 尚未实施。
    4.  **回调:**它定义了在训练期间要调用的回调列表。变量可以有一个或多个回调 onTrainBegin()、onTrainEnd()、onEpochBegin()、onEpochEnd()、onBatchBegin()、onBatchEnd()、onYield()。
    5.  **validationSplit:** 用户可以很容易地将训练数据集拆分为训练和验证。例如:如果它的值是 validation-Split = 0.5，则意味着在洗牌进行验证之前使用最后 50%的数据。
    6.  **验证数据:**用于在最终模型之间进行选择时给出最终模型的估计值。
    7.  **混洗:**该值定义了每个纪元前数据的混洗。当 stepsPerEpoch 不为空时，它不起作用。
    8.  **classWeight:** 用于对损失函数进行加权。告诉模型更多地关注来自表示不足的类的样本可能是有用的。
    9.  **样本权重:**这是应用于每个样本的模型损失的权重数组。
    10.  **initialEpoch:** 是定义开始训练的历元的值。这对于恢复之前的训练很有用。
    11.  **stepspereach:**在宣布一个纪元结束并开始下一个纪元之前，它定义了多个批次的样本。如果未确定，则等于 1。
    12.  **验证步骤:**如果指定了*步骤*，则相关。停止前要验证的步骤总数。
    13.  **yieldEvery:** 定义将主线程让给其他任务的频率的配置。它可以是自动的，这意味着屈服发生在一定的帧速率。批次，如果值是这个，它会产生每个批次。纪元，如果值是这个，它产生每个纪元。任何数字，如果值是任何数字，它会产生每一个数字*毫秒*。*永不*，如果值是这个，它就永不屈服。

**回归:**回归历史的承诺。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining model
const mymodel = tf.sequential({
     layers: [tf.layers.dense({units: 2, inputShape: [6]})]
});

// Compiling the above model
mymodel.compile({optimizer: 'sgd', loss: 'meanSquaredError'});

// Using for loop
for (let i = 0; i < 4; i++) {

  // Calling fit() method
  const his = await mymodel.fit(tf.zeros([6, 6]), tf.ones([6, 2]), {
       batchSize: 5,
       epochs: 4
   });

    // Printing output
    console.log(his.history.loss[1]);
}
```

**输出:**

```
0.9574100375175476
0.8151942491531372
0.694103479385376
0.5909997820854187
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining model
const mymodel = tf.sequential({
     layers: [tf.layers.dense({units: 2, inputShape: [6], 
                               activation : "sigmoid"})]});

// Compiling the above model
mymodel.compile({optimizer: 'sgd', loss: 'meanSquaredError'});   

// Calling fit() method
 const his = await mymodel.fit(tf.truncatedNormal([6, 6]), 
                             tf.randomNormal([6, 2]), { batchSize: 5,
                             epochs: 4, validationSplit: 0.2, 
                             shuffle: true, initialEpoch: 2, 
                             stepsPerEpoch: 1, validationSteps: 2});

// Printing output
console.log(JSON.stringify(his.history));
```

**输出:**

```
{"val_loss":[0.35800713300704956,0.35819053649902344],
"loss":[0.633269190788269,0.632409930229187]}
```

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.LayersModel.fit