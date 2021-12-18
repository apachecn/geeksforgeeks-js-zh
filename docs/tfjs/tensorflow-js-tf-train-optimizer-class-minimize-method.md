# tensorflow . js TF . train . optimizer 类。最小化()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-train-optimizer-class-minimum-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-train-optimizer-class-minimize-method/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**。最小化()**方法执行给定函数 **f()** ，并试图通过计算 y 相对于由**变量列表表示的给定可训练变量列表的梯度来最小化 **f()** 的标量输出。**如果没有提供列表，它计算所有可训练变量的梯度。

**语法:**

```
Optimizer.minimize (f, returnCost?, varList?)
```

**参数:**

*   **f (() = > tf。标量):**它指定要执行的函数和要最小化其输出的函数。
*   **returnCost(布尔值):**指定是否返回执行 f()产生的标量成本值。
*   **varList (tf。变量[]):** 指定可训练变量列表。

**返回值:** tf。标量| null

**例 1:**

## Javascript

```
// Importing tensorflow
import tensorflow as tf

const xs = tf.tensor1d([0, 1, 2]);
const ys = tf.tensor1d([1.3, 2.5, 3.7]);

const x = tf.scalar(Math.random()).variable();
const y = tf.scalar(Math.random()).variable();

// Define a function f(x, y) = x + y.
const f = x => x.add(y);
const loss = (pred, label) =>
    pred.sub(label).square().mean();

const learningRate = 0.05;

// Create adagrad optimizer
const optimizer =
  tf.train.adagrad(learningRate);

// Train the model.
for (let i = 0; i < 5; i++) {
   optimizer.minimize(() => loss(f(xs), ys));
}

// Make predictions.
console.log(
`x: ${x.dataSync()}, y: ${y.dataSync()}`);
const preds = f(xs).dataSync();
preds.forEach((pred, i) => {
console.log(`x: ${i}, pred: ${pred}`);
});
```

**输出**

```
x: 0.9395854473114014, y: 1.0498266220092773
x: 0, pred: 1.0498266220092773
x: 1, pred: 2.0498266220092773
x: 2, pred: 3.0498266220092773
```

**例二:**

## Javascript

```
// Importing tensorflow
import * as tf from "@tensorflow/tfjs"

const xs = tf.tensor1d([0, 1, 2, 3]);
const ys = tf.tensor1d([1.1, 5.9, 16.8, 33.9]);

// Choosing random coefficients
const a = tf.scalar(Math.random()).variable();
const b = tf.scalar(Math.random()).variable();
const c = tf.scalar(Math.random()).variable();

// Defining function f = (a*x^2 + b*x + c)
const f = x => a.mul(x.square()).add(b.mul(x)).add(c);
const loss = (pred, label) => pred.sub(label).square().mean();

// Setting configurations for our optimizer
const learningRate = 0.01;
const decay = 0.1;
const momentum = 1;
const epsilon = 0.5;
const centered = true;

// Create the ptimizer
const optimizer = tf.train.rmsprop(learningRate,
        decay, momentum, epsilon, centered);

// Train the model.
for (let i = 0; i < 8; i++) {
   optimizer.minimize(() => loss(f(xs), ys));
}

// Make predictions.
console.log(`a: ${a.dataSync()},
    b: ${b.dataSync()}, c: ${c.dataSync()}`);
const preds = f(xs).dataSync();
preds.forEach((pred, i) => {
   console.log(`x: ${i}, pred: ${pred}`);
});
```

**输出**

```
a: 3.6799352169036865, 
    b: 4.26292610168457, c: 4.544136047363281
x: 0, pred: 4.544136047363281
x: 1, pred: 12.486997604370117
x: 2, pred: 27.789730072021484
x: 3, pred: 50.45233154296875
```

**参考:**[https://js . tensorflow . org/API/latest/# TF . train . optimizer . minimum](https://js.tensorflow.org/api/latest/#tf.train.Optimizer.minimize)