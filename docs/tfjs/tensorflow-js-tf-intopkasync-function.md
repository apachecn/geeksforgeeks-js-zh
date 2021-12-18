# tensorlow . js TF . intpkasync()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-intpk-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。inTopKAsync()函数**用于检查所述目标是否在给定的顶部 K *预测*中。

**语法:**

```
tf.inTopKAsync(predictions, targets, k?)
```

**参数:**

*   **预测:**它是所述的二维或上张量输入，其最后大小不小于 *k* ，并且它可以是 tf 类型。张量、类型或数组。
*   **目标:**它是所述的一维或上张量输入，并且它可以是 tf 类型。张量、类型或数组。
*   **k:** 是计算精度需要考虑的顶层元素的可选数量。默认值为 1，并且是数字类型。

**返回值:**返回 Promise tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining predictions and targets
const pred = tf.tensor2d([
    [11, 22, 33, 55], 
    [33, 66, 22, -11]
]);

const targ = tf.tensor1d([1, 1]);

// Calling tf.inTopKAsync() method
const res = await tf.inTopKAsync(pred, targ);

// Printing output
res.print();
```

**输出:**

```
Tensor
    [false, true]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling tf.inTopKAsync() method with 
// all its parameters
const res = await tf.inTopKAsync(
    tf.tensor2d([[1.1, 2.2], [3.3, 6.6]]), 
    tf.tensor1d([0, 1]), 2);

// Printing output
res.print();
```

**输出:**

```
Tensor
    [true, true]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#inTopKAsync