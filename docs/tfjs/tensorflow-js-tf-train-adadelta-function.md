# tensorlow . js TF . train . adadelta()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-train-adadelta-function/

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**tf.train.adadelta()** 函数我们用来创建一个 tf。使用 adadelta 算法的 AdadeltaOptimizer。adadelta 算法是梯度下降优化算法的扩展。它用于优化神经网络。

**语法:**

```
tf.train.adadelta(learningRate)
```

**参数:**

*   **学习速率:**指定 adadelta 梯度下降算法将使用的学习速率。
*   **ρ:**它指定每次更新的学习速率衰减。
*   **ε:**它指定了一个常数ε，用于改善梯度更新的条件。可选择的

**返回值:**返回一个 tf.adadeltaOptimizer

**示例 1:** 通过学习系数 a 和 b，使用 adadelta 优化器拟合函数 f =(a * x+y).

## Javascript

```
// Importing tensorflow
import * as tf from "@tensorflow/tfjs"

const xs = tf.tensor1d([0, 1, 2, 3]);
const ys = tf.tensor1d([1.1, 5.9, 16.8, 33.9]);

// Choosing variable coefficients
const a = tf.scalar(Math.random()).variable();
const b = tf.scalar(Math.random()).variable();

// Defining function f = (a*x + b)
const f = x => a.mul(x).add(b);
const loss = (pred, label) => pred.sub(label).square().mean();

const learningRate = 0.01;

// Creating optimizer
const optimizer = tf.train.adadelta(learningRate);

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
a: 5.39164924621582, b: 1.8858184814453125}
x: 0, pred: 1.8858184814453125
x: 1, pred: 7.277467727661133
x: 2, pred: 12.669116973876953
x: 3, pred: 18.060766220092773
```

**示例 2:** 通过学习系数 a、b 和 c，使用 adadelta 优化器拟合二次方程。优化器配置如下:

*   Learning rate = 0.01
*   φ= 0.2
*   e= 0.5

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

// Setting configurations for our optimizer
const learningRate = 0.01;
const rho = 0.2;
const epsilon = 0.5;

// Creating the optimizer
const optimizer = tf.train.adadelta(learningRate, rho, epsilon);

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
a: 3.1871466636657715, b: 1.5096971988677979, c:0.8317463397979736
x: 0, pred: 0.8317463397979736
x: 1, pred: 5.528590202331543
x: 2, pred: 16.599727630615234
x: 3, pred: 34.04515838623047
```

**参考资料:**[https://js . tensorlow . org/API/1 . 0 . 0/# train . adadelta](https://js.tensorflow.org/api/1.0.0/#train.adadelta)