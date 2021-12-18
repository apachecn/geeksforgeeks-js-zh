# Tensorflow.js tf。顺序类。评估()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sequential-class-evaluate-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-sequential-class-evaluate-method/)

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
*   **Y:** is the stated tf. Tensor of the object, or an array of tf. Tensor in case the prototype has different output. It can be tf type. Or tensor tf. Tensor [].
*   **args:** It is said that [T2】 modelavalateargs 【T3] has an elective field. It is an object.
*   **Batch size:** is the specified batch size; if it is not defined, the default value is 32\. It's of numerical type.
*   **Detail:** is the mode of statement detail. Type *model detail* .
*   **Sample weight:** It is the weight tensor mentioned above, so as to weight the influence of various situations on the loss and the measurement. It is of type Tf.tensor.
*   **Steps:** It is the total number of steps before the declaration of the estimation wheel is terminated, that is, the instance group. It is ignored and the default value is unspecified. It's of numerical type.

**返回值:**返回 tf。标量或 tf。标量[]。

**示例 1:** 使用优化器作为“ *sgd* ”，使用损失作为“*意味着绝对错误*”。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining model
const modl = tf.sequential({
   layers: [tf.layers.dense({units: 3, inputShape: [40]})]
});

// Compiling model
modl.compile({optimizer: 'sgd', loss: 'meanAbsoluteError'});

// Calling evaluate() and randomNormal
// method
const output = modl.evaluate(
    tf.randomNormal([5, 40]), 
    tf.randomNormal([5, 3]), 
    {Sizeofbatch: 3}
);

// Printing output
output.print();
```

**输出:**

```
Tensor
    1.554270625114441
```

这里使用 randomNormal()方法作为张量输入。

**示例 2:** 使用优化器作为“*亚当*”，使用损失作为“*均值平方误差*”和“*精度*”作为度量。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining model
const modl = tf.sequential({
   layers: [tf.layers.dense({units: 2, inputShape: [30]})]
});

// Compiling model
modl.compile({optimizer: 'adam', loss: 'meanSquaredError'}, 
             (metrics = ["accuracy"]));

// Calling evaluate() and truncatedNormal
// method
const output = modl.evaluate(
     tf.truncatedNormal([6, 30]), tf.truncatedNormal([6, 2]), 
      {Sizeofbatch: 2}, {steps: 2});

// Printing output
output.print();
```

**输出:**

```
Tensor
    2.7340292930603027
```

这里，截断法线()方法用作张量输入，并且还包括步长参数。

**参考:**[https://js.tensorflow.org/api/latest/#tf.顺序评估](https://js.tensorflow.org/api/latest/#tf.Sequential.evaluate)