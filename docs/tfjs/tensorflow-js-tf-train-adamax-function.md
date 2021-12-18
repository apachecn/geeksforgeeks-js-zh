# tensorlow . js TF . train . adamax()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-train-adamax-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-train-adamax-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**tf.train.adamax()** 函数我们用来创建一个 tf。使用 adamax 算法的 AdamaxOptimizer。

**语法:**

```
tf.train.adamax(learningRate, beta1, beta2, epsilon, decay)
```

**参数:**

*   **学习速率:**指定 adamax 梯度下降算法将使用的学习速率。
*   **β1:**它指定了第一时刻的估计指数衰减率。
*   **β2:**指定第二时刻的估计指数衰减率。
*   **ε:**它为数值稳定性指定了一个小常数。
*   **衰减:**指定每次更新的衰减率。

**返回值:**返回一个 tf.adamaxOptimizer。

**示例 1:** 通过学习系数 a 和 b，使用 adamax 优化器拟合函数 f =(a * x+y).

## Javascript

```
// Importing tensorflow
import * as tf from "@tensorflow/tfjs"

const xs = tf.tensor1d([0, 1, 2, 3]);
const ys = tf.tensor1d([1.1, 5.9, 16.8, 33.9]);

// Choosing random coefficients
const a = tf.scalar(Math.random()).variable();
const b = tf.scalar(Math.random()).variable();

// Defining function f = (a*x + b).
const f = x => a.mul(x).add(b);
const loss = (pred, label) => pred.sub(label).square().mean();

// Defining learning rate of adamax algorithm
const learningRate = 0.01;

// Creating our optimizer.
const optimizer = tf.train.adamax(learningRate);

// Train the model.
for (let i = 0; i < 10; i++) {
   optimizer.minimize(() => loss(f(xs), ys));
}

// Make predictions.
console.log(
     `a: ${a.dataSync()}, b: ${b.dataSync()}}`);
const preds = f(xs).dataSync();
preds.forEach((pred, i) => {
   console.log(`x: ${i}, pred: ${pred}`);
});
```

**输出:**

```
a: 0.4271160364151001, b: 0.21284617483615875}
x: 0, pred: 0.21284617483615875
x: 1, pred: 0.6399621963500977
x: 2, pred: 1.0670782327651978
x: 3, pred: 1.4941942691802979
```

**示例 2:** 使用 adamax 优化器，通过学习系数 a、b 和 c 来拟合二次方程，我们的优化器的配置如下:

*   Learning rate = 0.01;
*   b1 = 0.1;
*   b2 = 0.1;
*   e= 0.3;
*   Decay = 0.5;

## Javascript

```
// Importing tensorflow
import * as tf from "@tensorflow/tfjs"

const xs = tf.tensor1d([0, 1, 2, 3]);
const ys = tf.tensor1d([1.1, 5.9, 16.8, 33.9]);

// Choosing random coefficients
const a = tf.scalar(Math.random()).variable();
const b = tf.scalar(Math.random()).variable();

// Defining function f = (a*x^2 + b*x + c).
const f = x => a.mul(x).add(b);
const loss = (pred, label) => pred.sub(label).square().mean();

// Defining configurations of adamax algorithm
const learningRate = 0.01;
const beta1 = 0.1;
const beta2 = 0.1;
const epsilon = 0.3;
const decay = 0.5;

// Creating our optimizer.
const optimizer = tf.train.adamax(
    learningRate, beta1, beta2, epsilon, decay);

// Train the model.
for (let i = 0; i < 10; i++) {
   optimizer.minimize(() => loss(f(xs), ys));
}

// Make predictions.
console.log(
     `a: ${a.dataSync()}, b: ${b.dataSync()}}`);
const preds = f(xs).dataSync();
preds.forEach((pred, i) => {
   console.log(`x: ${i}, pred: ${pred}`);
});
```

**输出:**

```
a: 0.8346626162528992, b: 0.5925931334495544}
x: 0, pred: 0.21284617483615875
x: 1, pred: 1.4272557497024536
x: 2, pred: 2.261918306350708
x: 3, pred: 3.096580982208252
```

**参考资料:**[https://js . tensorlow . org/API/1 . 0 . 0/# train . adamax](https://js.tensorflow.org/api/1.0.0/#train.adamax)