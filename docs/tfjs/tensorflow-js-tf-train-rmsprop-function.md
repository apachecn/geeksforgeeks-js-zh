# tensorflow . js TF . train . rmsprop()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-train-rmsprop-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-train-rmsprop-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**tf.train.rmsprop()** 函数用于创建一个 tf。RMSPropOptimizer，使用 RMSProp gradient 体面算法。RMSProp 优化器的实现并不是 RMSProp 的中心版本，它使用的是普通动量。

**语法:**

```
tf.train.rmsprop(learningRate, decay, momentum, epsilon, centered)
```

**参数:**

*   **学习率(数字):**指定 adadelta 梯度下降算法将使用的学习率。
*   **衰变(数):**指定各梯度的衰变速率。
*   **动量(数):**指定 rmsprop 梯度下降算法将使用的动量。
*   **ε:**它指定了一个恒定的小值，用于避免分母为零。
*   **居中(布尔值):**指定梯度是否由估计的梯度方差归一化。

**返回值:**返回一个 tf。RMSPropOptimizer

**示例 1:** 通过学习系数 a 和 b，使用 RMSProp 优化器拟合函数 f =(a * x+y).

## Javascript

```
// Importing tensorflow
import * as tf from "@tensorflow/tfjs"

const xs = tf.tensor1d([0, 1, 2]);
const ys = tf.tensor1d([1.1, 5.9, 16.8]);

// Choosing random coefficients.
const a = tf.scalar(Math.random()).variable();
const b = tf.scalar(Math.random()).variable();

// Defining function f = (a*x + b). We will use
// optimizer to fit f
const f = x => a.mul(x).add(b);
const loss = (pred, label) => pred.sub(label).square().mean();

// Define rate which will be used by rmsprop algorithm
const learningRate = 0.01;

// Create optimizer
const optimizer = tf.train.rmsprop(learningRate);

// Train the model.
for (let i = 0; i < 8; i++) {
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
a:0.9164762496948242, b: 1.0887205600738525}
x: 0, pred: 1.0887205600738525
x: 1, pred: 2.0051968097686768
x: 2, pred: 2.921673059463501
```

**示例 2:** 使用 RMSProp 优化器拟合一个二次方程，通过学习系数 a、b 和 c。优化器将具有以下配置:

*   Learning rate = 0.01
*   Attenuation = 0.1
*   Momentum = 1
*   e= 0.5
*   Center = true

## Javascript

T0

**输出:**

```
a: 3.918823003768921, b: 3.333444833755493, c: 6.297145843505859
x: 0, pred: 6.297145843505859
x: 1, pred: 13.549413681030273
x: 2, pred: 28.639328002929688
x: 3, pred: 51.56688690185547
```

**参考资料:**[https://js . tensorlow . org/API/1 . 0 . 0/# train . rmsprep](https://js.tensorflow.org/api/1.0.0/#train.rmsprop)