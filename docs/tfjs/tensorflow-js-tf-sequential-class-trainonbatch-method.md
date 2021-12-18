# Tensorflow.js tf。顺序类。列车批次()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sequential-class-trainenbatch-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-sequential-class-trainonbatch-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。trainOnBatch()函数**用于对特定批次的数据运行单独的梯度更新。

**注:**

该方法从*拟合*()以及*拟合数据集*()以下列方式变化:

*   这种方法绝对适用于一批数据。
*   该方法只返回损失和度量值，而不是逐批返回损失和度量值。
*   这种方法不支持像冗长和回调这样的细粒度选项。

**语法:**

```
trainOnBatch(x, y)
```

**参数:**

*   **x:** the input data. It can be tf type. Tensor. Tensor[], or {[inputName: string]: tf. Tensor. It can be any of the following:
    1.  Tf specified. Tensor, or an array of tf. Tensor if the model has multiple inputs.
    2.  Draw the input name to the object that matches tf. Tensor, in case the model has named input.
*   **Y:** The target data. It can be tf type. Tensor. Tensor[], or {[inputName: string]: tf. Tensor. It must be constant with respect to x.

**返回值:**返回数字或数字[]的承诺。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Training Model 
const gfg = tf.sequential();

// Adding layer to model  
const layer = tf.layers.dense({units:3, 
               inputShape : [5]});
   gfg.add(layer);

// Compiling our model 
const config = {optimizer:'sgd', 
              loss:'meanSquaredError'};
  gfg.compile(config);

// Test tensor and target tensor
const xs = tf.ones([3, 5]);
const ys = tf.ones([3, 3]);

// Calling trainOneBatch() method
const result = await gfg.trainOnBatch(xs, ys);

// Printing output
console.log(result);
```

**输出:**

```
0.3589147925376892
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

async function run() {

  // Training Model 
  const gfg = tf.sequential();

  // Adding layer to model  
  const layer = tf.layers.dense({units:2, 
               inputShape : [2]});
  gfg.add(layer);

  // Compiling our model 
  const config = {optimizer:'sgd', 
              loss:'meanSquaredError'};
  gfg.compile(config);

  // Test tensor and target tensor
  const xs = tf.truncatedNormal([3, 2]);
  const ys = tf.randomNormal([3, 2]);

  // Calling trainOneBatch() method
  const result = await gfg.trainOnBatch(xs, ys);

  // Printing output
  console.log(JSON.stringify(+result));
}

// Function call
await run();
```

**输出:**

```
1.6889342069625854
```

**参考:**[https://js.tensorflow.org/api/latest/#tf.顺序列车批次](https://js.tensorflow.org/api/latest/#tf.Sequential.trainOnBatch)