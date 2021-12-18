# tensorlow . js TF . train . Adam()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-train-Adam-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-train-adam-function/)

Tensorflow.js 是谷歌开发的一个 javascript 库，用于在浏览器或 Node.js 中运行和训练机器学习模型。

**Adam 优化器**(或自适应矩估计)是一种基于一阶和二阶矩自适应估计的随机梯度下降方法。优化技术在处理大量数据和参数时非常有效。更多详情请参考[文章](https://www.geeksforgeeks.org/intuition-of-adam-optimizer/)。

在 Tensorflow.js 中 **tf.train.adam()** 函数用于创建 tf。使用 adam 算法的 AdamOptimizer。

**语法:**

```
tf.train.adam (learningRate?, beta1?, beta2?, epsilon?)
```

**参数:**

*   **Learning rate:** Learning rate used for Adam gradient descent algorithm. It is *optional.*
*   [T0】 β1: 【T1: Estimation of exponential decay rate at the first moment. It is *optional.*
*   **β 2:** Estimation of exponential decay rate at the second time. It is *optional.*
*   [T0】 ε: 【T1] A small constant with stable numerical value. It is *optional.*

**返回值:** AdamOptimizer。

**例 1:** 以 x，y 输入张量和 A，b，c 为随机系数定义二次函数。然后，我们计算预测的均方损失，并将其传递给 adam 优化器，以最小化损失，并理想地更改系数。

## Javascript

```
// A cubic function with its coeffiecient l,m,n.
const x = tf.tensor1d([0, 1, 2, 3]);
const y = tf.tensor1d([1., 2., 5., 11.]);

const l = tf.scalar(Math.random()).variable();
const m = tf.scalar(Math.random()).variable();
const n = tf.scalar(Math.random()).variable();

// y = l * x^3 - m * x + n.
const f = x => l.mul(x.pow(3)).sub(m.mul(x)).add(n);
const loss = (pred, label) => pred.sub(label).square().mean();

const learningRate = 0.01;
const optimizer = tf.train.adam(learningRate);

// Training the model and printing the coefficients.
for (let i = 0; i < 10; i++) {
   optimizer.minimize(() => loss(f(x), y));
  console.log(
     `l: ${l.dataSync()}, m: ${m.dataSync()}, n: ${n.dataSync()}`);
}

// Predictions are made.

const preds = f(x).dataSync();
preds.forEach((pred, i) => {
   console.log(`x: ${i}, pred: ${pred}`);
});
```

**输出:**

```
l: 0.5212615132331848, m: 0.4882013201713562, n: 0.9879841804504395
l: 0.5113212466239929, m: 0.49809587001800537, n: 0.9783468246459961
l: 0.5014950633049011, m: 0.5077731013298035, n: 0.969675600528717
l: 0.49185076355934143, m: 0.5170749425888062, n: 0.9630305171012878
l: 0.48247095942497253, m: 0.5257879495620728, n: 0.9595866799354553
l: 0.47345229983329773, m: 0.5336435437202454, n: 0.9596782922744751
l: 0.4649032950401306, m: 0.5403363704681396, n: 0.9626657962799072
l: 0.4569399356842041, m: 0.5455683469772339, n: 0.9677067995071411
l: 0.4496782124042511, m: 0.5491118431091309, n: 0.9741682410240173
l: 0.44322386384010315, m: 0.5508641004562378, n: 0.9816395044326782
x: 0, pred: 0.9816395044326782
x: 1, pred: 0.8739992380142212
x: 2, pred: 3.4257020950317383
x: 3, pred: 11.29609203338623
```

**示例 2:** 下面是我们设计一个简单模型的代码，我们通过 **tf.train.adam** 定义一个学习率参数为 0.01 的优化器，并将其传递给模型编译。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// defining the model
const model = tf.sequential({
    layers: [tf.layers.dense({ units: 1, inputShape: [12] })],
});

// in the compilation we use tf.train.adam optimizer
  const optimizer = tf.train.adam(0.001);
model.compile({ optimizer: optimizer, loss: "meanSquaredError" },
              (metrics = ["accuracy"]));

// evaluate the model which was compiled above
const result = model.evaluate(tf.ones([10, 12]), tf.ones([10, 1]), {
    batchSize: 4,
});

// print the result
result.print();
```

**输出:**

```
Tensor
    1.520470142364502
```

**参考资料:**[https://js . tensorlow . org/API/3 . 6 . 0/# train . Adam](https://js.tensorflow.org/api/3.6.0/#train.adam)