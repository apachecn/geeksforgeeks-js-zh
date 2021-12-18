# Tensorflow.js tf。LayersModel 类。列车批次()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers model-class-trainenbatch-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layersmodel-class-trainonbatch-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。trainOnBatch()函数**用于对特定批次的数据运行单独的梯度更新。

**注:**该方法与*拟合*()以及*拟合数据集*()的不同之处在于:

*   This method is absolutely suitable for a batch of data.
*   This method only returns loss and measure values, instead of batch by batch.
*   This method does not support fine-grained options such as verbosity and callback.

**语法:**

```
trainOnBatch(x, y)
```

**参数:**

*   **x:** the input data. It can be tf type. Tensor. Tensor[], or {[inputName: string]: tf. Tensor. It can be any of the following:
    1.  Tf specified. Tensor, or an array of tf. Tensor if the model has multiple inputs.
    2.  Draw the input name to the object that matches tf. Tensor, in case the model has named input.
*   **Y:** The target data. It can be tf type. Tensor. Tensor[], or {[inputName: string]: tf. Tensor. It must remain the same relative to *x* .

**返回值:**返回数字或数字[]的承诺。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Training Model
const mymodel = tf.sequential(
     {layers: [tf.layers.dense({units: 2, inputShape: [2]})]});

// Compiling our model
const config = {optimizer:'sgd',
            loss:'meanSquaredError'};
mymodel.compile(config);

// Test tensor and target tensor
const xs = tf.ones([3,2]);
const ys = tf.ones([3,2]);

// Calling trainOneBatch() method
const result = await mymodel.trainOnBatch(xs, ys);

// Printing output
console.log(result);
```

**输出:**

```
2.0696773529052734
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

async function run() {

  // Training Model
  const mymodel = tf.sequential(
     {layers: [tf.layers.dense({units: 2, inputShape: [2], 
                                activation: 'sigmoid'})]});

  // Compiling our model
  const config = {optimizer:'sgd',
            loss:'meanSquaredError'};
  mymodel.compile(config);

  // Test tensor and target tensor
  const xs = tf.truncatedNormal([3,2]);
  const ys = tf.randomNormal([3,2]);

  // Calling trainOneBatch() method
  const result = await mymodel.trainOnBatch(xs, ys);

  // Printing output
  console.log(JSON.stringify(+result));
}

// Function call
await run();
```

**输出:**

```
0.5935208797454834
```

**参考:**[https://js.tensorflow.org/api/latest/#tf.layer model . trainionbatch](https://js.tensorflow.org/api/latest/#tf.LayersModel.trainOnBatch)