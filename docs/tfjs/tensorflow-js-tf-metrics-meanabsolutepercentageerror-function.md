# tensorflow . js TF . metrics . meanusolutepercentageerror()函数

> 原文:[https://www . geeksforgeeks . org/tensorflow-js-TF-metrics-meanusolutepercentageerror-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-metrics-meanabsolutepercentageerror-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**. metrics . mean absolutePercentageerror()****函数**是一个损失或其他度量函数，即平均绝对百分比误差，它使用真值和预测张量输入来返回 tf。张量对象。

**语法:**

```
tf.metrics.meanAbsolutePercentageError(yTrue, yPred)
```

**参数:**

*   **yTrue:** 是陈述的真张量，可以是 tf.Tensor 类型
*   **yPred:** 是所述的预测张量，可以是 tf.Tensor 类型

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining truth and prediction tensors
const y = tf.tensor2d([[0, 2], [20, 30]]);
const z = tf.tensor2d([[0, 2], [21, 34]]);

// Calling metrics.meanAbsolutePercentageError() 
// method
const mape = tf.metrics.meanAbsolutePercentageError(y, z);

// Printing output
mape.print();
```

**输出:**

```
Tensor
    [0, 9.166666]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling metrics.meanAbsolutePercentageError() 
// method with its parameter directly and then
// Printing output
const output = tf.metrics.meanAbsolutePercentageError(tf.tensor(
    [
      [0, 1, 0, 0],
      [0, 1, 1, 0],
      [0, 0, 0, 1],
      [1, 1, 0, 0],
      [0, 0, 1, 0]
    ]
), tf.tensor(
    [
      [0, 0, 1, 1],
      [0, 1, 1, 0],
      [0, 0, 0, 1],
      [0, 1, 0, 1],
      [1, 1, 0, 0]
    ]
)).print();
```

**输出:**

```
Tensor
    [500025, 0, 0, 250025, 500025]
```

**参考:**[https://js . tensorflow . org/API/latest/# metrics . measuresultepercentageerror](https://js.tensorflow.org/api/latest/#metrics.meanAbsolutePercentageError)