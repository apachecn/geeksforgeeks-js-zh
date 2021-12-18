# tensorflow . js TF . train . optimizer 类。计算组件()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-train-optimizer-class-computegaledints-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-train-optimizer-class-computegradients-method/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

执行 f()并计算 f()的标量输出相对于*变量列表*提供的可训练变量列表的梯度。如果没有提供列表，默认为所有可训练变量。

**语法:**

```
Optimizer.computeGradients(f, varList?);
```

**参数:**

*   **f ( ( ) = > tf。标量):**要执行的函数，其输出用于计算变量的梯度。
*   **varLIst( tf。变量[ ] ):** 计算梯度的可选变量列表。如果指定，只有可训练变量是 varList，将根据计算梯度。默认为所有可训练变量。

**返回:** {值:tf。标量，梯度:{ [名称:字符串] : tf。张量} }

**例 1:**

## Javascript

```
// Importing tensorflow
import * as tf from "@tensorflow/tfjs"

const xs = tf.tensor1d([3, 4, 5]);
const ys = tf.tensor1d([3.5, 4.7, 5.3]);

const x = tf.scalar(Math.random()).variable();
const y = tf.scalar(Math.random()).variable();

// Define a function f(x, y) = ( x^2 ) -  y.
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

**例二:**

## Javascript

```
// Importing tensorflow
import * as tf from "@tensorflow/tfjs"

const xs = tf.tensor1d([0, 1, 2, 3]);
const ys = tf.tensor1d([1.3, 3.7, 12.4, 26.6]);

// Choosing random coefficients
const a = tf.scalar(Math.random()).variable();
const b = tf.scalar(Math.random()).variable();
const c = tf.scalar(Math.random()).variable();

// Defining function f = (a*x^2 + b*x + c)
const f = x => a.mul(x.mul(3)).add(b.square(x)).add(c);
const loss = (pred, label) => pred.sub(label).square().mean();

// Setting configurations for our optimizer
const learningRate = 0.01;
const initialAccumulatorValue = 10;

// Create the Optimizer
const optimizer = tf.train.adagrad(learningRate,
        initialAccumulatorValue);

// Train the model.
for (let i = 0; i < 5; i++) {
optimizer.computeGradients(() => loss(f(xs), ys));
}

// Make predictions.
console.log(`a: ${a.dataSync()},
    b: ${b.dataSync()}, c: ${c.dataSync()}`);
const preds = f(xs).dataSync();
preds.forEach((pred, i) => {
console.log(`x: ${i}, pred: ${pred}`);
});
```

**输出:**

```
a: 0.22211307287216187,
b: 0.2304522693157196,
c: 0.42621928453445435
x: 0, pred: 0.479327529668808
x: 1, pred: 1.1456668376922607
x: 2, pred: 1.8120059967041016
x: 3, pred: 2.4783451557159424
```

**参考:**[https://js . tensorflow . org/API/latest/# TF . train . optimizer . computegredients](https://js.tensorflow.org/api/latest/#tf.train.Optimizer.computeGradients)