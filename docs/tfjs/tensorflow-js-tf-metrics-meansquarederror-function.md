# tensorflow . js TF . metrics . mean squarederor()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-metrics-mean squarederror-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-metrics-meansquarederror-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

张量流**函数是一个损失或度量函数，用于计算 y_true 和 y_pred 之间的均方误差。y_true 是真张量，y_pred 是预测张量。**

**语法:**

```
tf.metrics.meanSquaredError(tensor1, tensor2);
```

**参数:**该函数接受两个参数，如下图所示:

*   **张量 1:** 是真张量(y_true)。
*   **张量 2:** 是预测张量(y_pred)。

**返回值:**返回真值张量和预测张量之间的均方误差张量。

**例 1:**

## java 描述语言

```
// Importing the tensorflow.Js library
// import * as tf from "@tensorflow/tfjs"

// Creating the tensor
let truth = tf.tensor1d([6, 4]);
let prediction = tf.tensor1d([-3, -4]);

// Calculating mean squared Error
// between truth and prediction tensor
const mse = tf.metrics.meanSquaredError(truth, prediction);

// Printing mean square error
mse.print();
```

**输出:**

```
Tensor
    72.5
```

**例 2:**

## java 描述语言

```
// Importing the tensorflow.Js library
// import * as tf from "@tensorflow/tfjs"

// Calculating mean squared Error between
// truth and prediction tensor
let mse = tf.metrics.meanSquaredError(
    tf.tensor1d([0, 1, 2, 3]),
    tf.tensor1d([-8,-9, -10, -11])
);

// Printing mean square error
mse.print();
```

**输出:**

```
Tensor
    126
```

**参考:**[https://js . tensorflow . org/API/latest/# metrics . mean squarederor](https://js.tensorflow.org/api/latest/#metrics.meanSquaredError)