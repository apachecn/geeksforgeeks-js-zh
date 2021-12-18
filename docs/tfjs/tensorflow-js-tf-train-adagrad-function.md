# tensorlow . js TF . train . adagrad()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-train-adagrad-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.train.adagrad()** 函数我们用来创建一个 tf。使用自适应梯度算法的自适应梯度优化器。

**语法:**

```
tf.train.adagrad(learningRate).
```

**参数:**

*   **学习速率:**指定自适应梯度下降算法将使用的学习速率。
*   **initialacalculartorvalue:**指定累加器的初始值。肯定是正面的。

**返回值:**返回一个 tf.adagradOptimizer。

**示例 1 :** 通过学习系数 x，y 来拟合函数 f =(x+y).

## Javascript

```
// importing tensorflow
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
x: 0.8561810255050659, y: 0.6922483444213867
x: 0, pred: 0.6922483444213867
x: 1, pred: 1.6922483444213867
x: 2, pred: 2.6922483444213867
```

**示例 2:** 通过学习系数 a、b、c 来拟合二次函数。

## Javascript

```
// importing tensorflow
import tensorflow as tf

const xs = tf.tensor1d([0, 1, 2, 3]);
const ys = tf.tensor1d([1.1, 5.9, 16.8, 33.9]);

const a = tf.scalar(Math.random()).variable();
const b = tf.scalar(Math.random()).variable();
const c = tf.scalar(Math.random()).variable();

const f = x => a.mul(
  x.square()).add(b.mul(x)).add(c);
const loss = (pred, label) => 
         pred.sub(label).square().mean();

const learningRate = 0.01;
const optimizer = 
      tf.train.adagrad(learningRate);

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

**输出**

```
a: 0.3611285388469696, 
b: 0.6980878114700317, 
c: 0.8787991404533386
x: 0, pred: 0.8787991404533386
x: 1, pred: 1.9380154609680176
x: 2, pred: 3.7194888591766357
x: 3, pred: 6.223219394683838
```

**参考资料:**[https://js . tensorlow . org/API/1 . 0 . 0/# train . adagrad](https://js.tensorflow.org/api/1.0.0/#train.adagrad)