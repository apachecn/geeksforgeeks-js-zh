# Tensorflow.js tf。图层模型类。评估()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers model-class-evaluate-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layersmodel-class-evaluate-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。evaluate()函数**用于在测试方法中找到有利于原型的损失度量和度量值。

**注意:**

*   Here, the Loss value and metric are determined at compile time, that is, they need to be done before calling the evaluate () method.
*   The enumeration here is carried out in groups.

**语法:**

```
evaluate(x, y, args?)
```

**参数:**

*   **x:** is the prescribed tf. Tensor of test material, or array of tf. Tensor in case the prototype has different input. It can be tf type. Or tensor tf. Tensor [].
*   **Y:** is the stated tf. Tensor of the object, or an array of tf. Tensor in case the prototype has different input. It can be tf type. Or tensor tf. Tensor [].
*   **args:** It is said that [T2】 modelavalateargs 【T3] has an elective field. It is an object.
*   **Batch size:** is the specified batch size; if it is not defined, the default value is 32\. It's of numerical type.
*   **Detail:** is the mode of statement detail. Type *model detail* .
*   **Sample weight:** It is the weight tensor mentioned above, so as to weight the influence of various situations on the loss and the measurement. It is of type Tf.tensor.
*   **Steps:** It is the total number of steps before the declaration of the estimation wheel is terminated, that is, the instance group. It is ignored and the default value is unspecified. It's of numerical type.

**返回值:**返回 tf。标量或 tf。标量[]。

**示例 1:** 使用优化器作为“sgd”，使用损失作为“意味着绝对错误”。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining model
const modl = tf.sequential({
   layers: [tf.layers.dense({units: 2, inputShape: [30]})]
});

// Compiling model
modl.compile({optimizer: 'sgd', loss: 'meanAbsoluteError'});

// Calling evaluate() and randomNormal
// method
const output = modl.evaluate(
     tf.randomNormal([8, 30]), 
     tf.randomNormal([8, 2]), 
     {Sizeofbatch: 3}
);

// Printing output
output.print();
```

**输出:**这里，使用 *randomNormal()* 方法作为张量输入。

```
Tensor
    1.1059763431549072
```

**示例 2:** 使用优化器作为“亚当”，使用损失作为“均值平方误差”，使用“准确性”作为度量。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining model
const modl = tf.sequential({
   layers: [tf.layers.dense({units: 1, inputShape: [20]})]
});

// Compiling model
modl.compile({optimizer: 'adam', loss: 'meanSquaredError'}, 
             (metrics = ["accuracy"]));

// Calling evaluate() and truncatedNormal
// method
const output = modl.evaluate(
     tf.truncatedNormal([8, 20]), tf.truncatedNormal([8, 1]), 
      {Sizeofbatch: 3}, {steps: 2});

// Printing output
output.print();
```

**输出:**这里，使用*截断法线()*方法作为张量输入，还包括*步骤*参数。

```
Tensor
    1.2484867572784424
```

**参考:**[https://js.tensorflow.org/api/latest/#tf.图层模型评估](https://js.tensorflow.org/api/latest/#tf.LayersModel.evaluate)