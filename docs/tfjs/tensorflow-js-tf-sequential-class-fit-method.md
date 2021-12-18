# Tensorflow.js tf。顺序类。配合()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sequential-class-fit-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-sequential-class-fit-method/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

Tensorflow.jstf.Sequential 类。fit()方法用于为固定数量的时期(数据集上的迭代)训练模型。

**语法:**

```
model.fit( x, y, args?);
```

**参数:**该方法接受以下参数:

*   **x:** 是 tf。包含所有输入数据的张量。
*   **y:** 是 tf。包含所有输出数据的张量。
*   **参数:**是对象类型，变量如下:
    *   **batchSize:** 它定义将通过训练传播的样本数量。
    *   **时期:**它定义了训练数据数组的迭代。
    *   **详细:**它有助于显示每个纪元的进度。
        如果该值为 0，则表示在 fit()呼叫期间没有打印消息。如果值为 1–这意味着在 Node-js 中，它会打印进度条。在浏览器中，它不显示任何操作。值 1 是默认值。2–值 2 尚未实施。
    *   **回调:**它定义了在训练期间要调用回调列表。变量可以有一个或多个回调 onTrainBegin()、onTrainEnd()、onEpochBegin()、onEpochEnd()、onBatchBegin()、onBatchEnd()、onYield()。
    *   **validationSplit:** 用户可以轻松地将训练数据集拆分为训练和验证。
        例如:如果它的值是 validation-Split = 0.5，则表示使用洗牌前最后 50%的数据进行验证。
    *   **验证数据:**用于在最终模型之间进行选择时给出最终模型的估计值。
    *   **混洗:**该值定义每个时期之前数据的混洗。当步长值不为空时，它不起作用。
    *   **classWeight:** 用于对损失函数进行加权。告诉模型更多地关注来自表示不足的类的样本可能是有用的。
    *   **样本权重:**是应用于每个样本的模型损失的权重数组。
    *   **initialEpoch:** 是定义开始训练的历元的值。这对于恢复之前的训练很有用。
    *   **stepspereach:**定义在宣布一个纪元结束并开始下一个纪元之前的样品批次数量。如果未确定，则等于 1。
    *   **有效性步骤:**如果指定了步骤时间，则它是相关的。停止前要验证的步骤总数。
    *   **yieldeert:**定义将主线程让给其他任务的频率配置。它可以是自动的，这意味着屈服发生在一定的帧速率。批次，如果值是这个，它会产生每个批次。纪元，如果值是这个，它会产生每个纪元。任何数字，如果值是任何数字，它每毫秒产生一个数字。从不，如果值是这个，它从不产生。

**回报:**承诺<历史>

**示例 1:** 在本例中，我们将通过默认配置来训练我们的模型。

## java 描述语言

```
import * as tf from "@tensorflow/tfjs"

// Creating model
const model = tf.sequential( ) ;

// Adding layer to model
const config = {units: 1, inputShape: [1]}
const x = tf.layers.dense(config);
model.add(x);

// Compiling the model
const config2 = {optimizer: 'sgd', loss: 'meanSquaredError'}
model.compile(config2);

// Tensor for training
const xs = tf.tensor2d([1, 1.2,1.65, 1.29, 1.4, 1.7], [6, 1]);
const ys = tf.tensor2d([1, 0.07,0.17, 0.29, 0.43, 1.02], [6, 1]);

// Training the model
const Tm = await model.fit(xs, ys);

// Printing the loss after training
console.log("Loss  " + " : " + Tm.history.loss[0]);
```

**输出:**

```
Loss after Epoch  : 2.8400533199310303
```

**示例 2:** 在这个示例中，我们将通过进行一些配置来训练我们的模型。

## java 描述语言

```
import * as tf from "@tensorflow/tfjs"

// Creating model
const Model = tf.sequential( ) ;

// Adding layer to model
const config = {units: 4, inputShape: [2],
                activation : "sigmoid"}
const x = tf.layers.dense(config);
Model.add(x);

const config2 = {units: 3,
        activation : "sigmoid"}
const y = tf.layers.dense(config2);
Model.add(y);

// Compiling the model
const sgdOpt = tf.train.sgd(0.6)
const config3 = {optimizer: 'sgd', loss: 'meanSquaredError'}
Model.compile(config3);

// Test Tensor
const xs = tf.tensor2d([ [0.3, 0.24],
                        [0.12, 0.73],
                        [0.9, 0.54]
                        ]);

const ys = tf.tensor2d([ [0.43, 0.5, 0.92],
                        [0.1, 0.39, 0.12],
                        [0.76, 0.4, 0.92]
                        ]);

// Training the model
for( let i = 0; i < 5; i++){
const config = { shuffle : true, epoch : 10 }
const Tm = await Model.fit(xs, ys, config);

// Printing the loss after training
console.log("Loss " + " : " + Tm.history.loss[0]);

}
```

**输出:**

```
Loss   : 0.1362573206424713
Loss   : 0.13617873191833496
Loss   : 0.13610021770000458
Loss   : 0.13602176308631897
Loss   : 0.13594339787960052
```

**参考:**T2】https://js.tensorflow.org/api/3.8.0/#tf.Sequential.fit