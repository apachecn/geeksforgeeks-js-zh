# tensorflow . js TF . util . flat()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-util-flat-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-util-flatten-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**util .扁平化()函数**用于扁平化嵌套的不一致数组。

**语法:**

```
tf.util.flatten(arr, result?, skipTypedArray?)
```

**参数:**

*   **arr:** 要展平的是所述嵌套数组。它可以是类型号、布尔值、字符串、承诺<号>、类型号、递归类型号或类型号>。
*   **结果:**携带元素的是指定的目标数组。它是可选参数，可以是数字、布尔值、字符串、承诺<数字>、类型达瑞[]。
*   **skipTypedArray:** 是防止类型化数组扁平化的可选参数。而它的默认值是*假*。

**返回值:**可以返回数字、布尔值、字符串、承诺<数字>或类型达瑞[]。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining nested array
const arr = [[11, 12], [13, 14], [15, [16, [17]]]];

// Calling tf.util.flatten() method
const res = tf.util.flatten(arr);

// printing output
console.log(res);
```

**输出:**

```
11,12,13,14,15,16,17
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining nested array
const arr = [[11, 12], [13, 14], [15, [16, [17]]]];

// Defining destination array
const des_arr = [9, 10]

// Calling tf.util.flatten() method with
// all its parameters
const res = tf.util.flatten(arr, des_arr, true);

// printing output
console.log(res);
```

**输出:**

```
9,10,11,12,13,14,15,16,17
```

**参考资料:**[https://js . tensorlow . org/API/1 . 0 . 0/# flatten](https://js.tensorflow.org/api/1.0.0/#flatten)