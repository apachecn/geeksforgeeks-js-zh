# tensorflow . js TF . train . optimizer 类

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-train-optimizer-class/](https://www.geeksforgeeks.org/tensorflow-js-tf-train-optimizer-class/)

[Tensorflow.js](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。 **tf.train.Optimizer()类**用于扩展 Serializable 类。

这个 tf.train.Optimizer()类包含三个内置函数，如下所示。

*   tf.train.Optimizer()类[.最小化()](https://www.geeksforgeeks.org/tensorflow-js-tf-train-optimizer-class-minimize-method/)功能

[。computeGradients()](https://www.geeksforgeeks.org/tensorflow-js-tf-train-optimizer-class-computegradients-method/) 

*   Tf.train.Optimizer () class [. Apply the gradient ()](https://www.geeksforgeeks.org/tensorflow-js-tf-train-optimizer-class-applygradients-method/) function

**tf.train.Optimizer()类。最小化()**函数用于执行给定的函数 f()，并通过计算 y 相对于由*变量列表*表示的给定可训练变量列表的梯度来最小化 f()的标量输出。此外，如果没有提供列表，它会计算所有可训练变量的梯度。

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

**输出:**

```
x: 0.9395854473114014, y: 1.0498266220092773
x: 0, pred: 1.0498266220092773
x: 1, pred: 2.0498266220092773
x: 2, pred: 3.0498266220092773
```

**示例 2:**TF . train . optimizer()类。computeGradients()函数用于执行 f()，并计算 f()的标量输出相对于 varList 提供的可训练变量列表的梯度。此外，如果没有提供列表，它默认为所有可训练的变量。

## Javascript

```
// Importing tensorflow
import * as tf from "@tensorflow/tfjs"

const xs = tf.tensor1d([3, 4, 5]);
const ys = tf.tensor1d([3.5, 4.7, 5.3]);

const x = tf.scalar(Math.random()).variable();
const y = tf.scalar(Math.random()).variable();

// Define a function f(x, y) = ( x^2 ) - y.
const f = x => (x.square()).sub(y);
const loss = (pred, label) =>
    pred.sub(label).square().mean();

const learningRate = 0.05;

// Create adam optimizer
const optimizer =
tf.train.adam(learningRate);

// Train the model.
for (let i = 0; i < 6; i++) {
optimizer.computeGradients(() => loss(f(xs), ys));
}

// Make predictions.
console.log(
`x: ${x.dataSync()}, y: ${y.dataSync()}`);
const preds = f(xs).dataSync();
preds.forEach((pred, i) => {
console.log(`x: ${i}, pred: ${pred}`);
});
```

**输出:**

```
x: 0.38272422552108765, y: 0.7651948928833008
x: 0, pred: 8.2348051071167
x: 1, pred: 15.2348051071167
x: 2, pred: 24.234806060791016
```

**示例 3:**TF . train . optimizer()类。函数的作用是:使用计算出的梯度来更新变量。

## Javascript

```
// Importing tensorflow
 import * as tf from "@tensorflow/tfjs"

 const xs = tf.tensor1d([0, 1, 2]);
 const ys = tf.tensor1d([1.58, 2.24, 3.41]);

 const x = tf.scalar(Math.random()).variable();
 const y = tf.scalar(Math.random()).variable();

 // Define a function f(x) = x^2 + y.
 const f = x => (x.square()).add(y);

 const learningRate = 0.05;

 // Create adagrad optimizer
 const optimizer =
 tf.train.rmsprop(learningRate);

 // Updating variable
 const varGradients = f(xs).dataSync();
 for (let i = 0; i < 5; i++){
 optimizer.applyGradients(varGradients);
 }

 // Make predictions.
 console.log(
 `x: ${x.dataSync()}, y: ${y.dataSync()}`);
 const preds = f(xs).dataSync();
 preds.forEach((pred, i) => {
 console.log(`x: ${i}, pred: ${pred}`);
});
```

**输出:**

```
x: -0.526353657245636, y: 0.15607579052448273
x: 0, pred: 0.15607579052448273
x: 1, pred: 1.1560758352279663
x: 2, pred: 4.156075954437256
```

**参考:**T2】https://js.tensorflow.org/api/latest/#class:train.Optimizer