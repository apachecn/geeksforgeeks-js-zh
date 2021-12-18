# Tensorflow.js tf.train .动量()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-train-动量-函数/](https://www.geeksforgeeks.org/tensorflow-js-tf-train-momentum-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**tf . train . momentum()**函数用于创建一个 TF。使用动量梯度体面算法的动量优化器。

**语法:**

```
tf.train.momentum(learningRate, momentum, useNesterov)
```

**参数:**

*   **学习率(数字):**指定动量梯度下降算法将使用的学习率。
*   **动量(数):**指定动量梯度下降算法将使用的动量。
*   **使用 Nesterov(布尔值):**指定是否使用 nesterov 动量。这是一个可选参数。

**返回值:**返回一个 tf。动量优化器

**示例** **1:** 通过学习系数 a 和 b，使用动量优化器拟合函数 f=(a*x+b)。在本例中，我们将使用 nesterov 动量。所以使用水下机器人将是真的。

## Javascript

```
// Importing tensorflow
import * as tf from "@tensorflow/tfjs"

const xs = tf.tensor1d([0, 1, 2]);
const ys = tf.tensor1d([1.1, 5.9, 16.8]);

const a = tf.scalar(Math.random()).variable();
const b = tf.scalar(Math.random()).variable();

const f = x => a.mul(x).add(b);
const loss = (pred, label) => pred.sub(label).square().mean();

const learningRate = 0.01;
const momentum = 10;
const useNestrov = true;
const optimizer = tf.train.momentum(learningRate, momentum, useNestrov);

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
a: 1982014720, b:1076448384
x: 0, pred: 1076448384
x: 1, pred: 3058463232
x: 2, pred: 5040477696
```

**示例** **2:** 通过学习系数 a 和 b，使用动量优化器拟合二次方程。在此示例中，我们将不使用 nesterov 动量。所以 useNestrov 将是假的。

## Javascript

```
// Importing tensorflow
import * as tf from "@tensorflow/tfjs"

const xs = tf.tensor1d([0, 1, 2, 3]);
const ys = tf.tensor1d([1.1, 5.9, 16.8, 33.9]);

const a = tf.scalar(Math.random()).variable();
const b = tf.scalar(Math.random()).variable();
const c = tf.scalar(Math.random()).variable();

const f = x => a.mul(x.square()).add(b.mul(x)).add(c);
const loss = (pred, label) => pred.sub(label).square().mean();

const learningRate = 0.01;
const momentum = 10;
const useNestrov = false;
const optimizer = tf.train.momentum(learningRate, momentum, useNestrov);

// Train the model.
for (let i = 0; i < 10; i++) {
   optimizer.minimize(() => loss(f(xs), ys));
}

// Make predictions.
console.log(
     `a: ${a.dataSync()}, b: ${b.dataSync()}, c: ${c.dataSync()}`);
const preds = f(xs).dataSync();
preds.forEach((pred, i) => {
   console.log(`x: ${i}, pred: ${pred}`);
});
```

**输出:**

```
a: 892235776, b: 331963616, c: 134188384
x:0, pred: 134188384
x:1, pred: 1358387840
x:2, pred: 4367058944
x:3, pred: 9160201216
```

**参考:**T2】https://js.tensorflow.org/api/1.0.0/#train.momentum