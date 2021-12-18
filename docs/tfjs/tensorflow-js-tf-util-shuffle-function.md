# tensorflow . js TF . util . shuffle()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-util-shuffle-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-util-shuffle-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**.util.shuffle()函数**用于在 Fisher-Yates 算法的帮助下按顺序对所述数组进行洗牌。

**语法:**

```
tf.util.shuffle(array)
```

**参数:**

*   **数组:**是所述的要混洗的数组。它可以是 tf.any()[]、Uint32Array、int32Array 或 Float32Array 类型。

**返回值:**返回 void。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining array
const arr = [11, 12, 13, 14, 15];

// Calling tf.util.shuffle() method and
// printing output
tf.util.shuffle(arr);
console.log(arr);
```

**输出:**

```
14,12,11,13,15
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining array of float values
const arr = [1.1, 1.2, 1.3, 1.4, 1.5];

// Calling tf.util.shuffle() method and
// printing output
tf.util.shuffle(arr);
console.log(arr);
```

**输出:**

```
1.5,1.2,1.3,1.1,1.4

```

**参考:**https://js.tensorflow.org/api_node/2.0.1/#util.shuffle