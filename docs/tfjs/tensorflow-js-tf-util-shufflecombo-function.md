# tensorflow . js TF . util . shufflecombo()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-util-shufflecombo-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-util-shufflecombo-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**.util.shuffleCombo()** 函数用于在 Fisher-Yates 算法的帮助下按顺序对两个所述数组进行洗牌。

**语法:**

```
tf.util.shuffleCombo (array, array2)
```

**参数:**

*   **数组 1:** 是所述的第一个要混洗的数组。它可以是 tf.any()[]、Uint32Array、int32Array 或 Float32Array 类型。
*   **数组 2:** 所述第二个数组将被混洗。它可以是 tf.any()[]、Uint32Array、int32Array 或 Float32Array 类型。此外，它用与第一个所述数组等价的置换进行混洗。

**返回值:**返回 void。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining first and second array
const arr = [11, 12, 13, 14, 15];
const arr2 = [16, 17, 18, 19, 20];

// Calling tf.util.shuffleCombo() method and
// printing output
tf.util.shuffleCombo(arr, arr2);
console.log(arr, arr2);
```

**输出:**

```
12,14,11,15,13 17,19,16,20,18
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining first and second array 
// of float values
const arr = [4.5, 6.8, 17.1, 21.23, 45.8];
const arr2 = [47.9, 50.4, 52.5, 62.6, 73.7];

// Calling tf.util.shuffleCombo() method and
// printing output
tf.util.shuffleCombo(arr, arr2);
console.log(arr, arr2);
```

**输出:**

```
17.1,21.23,45.8,4.5,6.8 52.5,62.6,73.7,47.9,50.4
```

**参考:**T2】https://js.tensorflow.org/api/latest/#util.shuffleCombo