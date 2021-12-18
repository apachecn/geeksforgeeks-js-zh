# Tensorflow.js tf.unique()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-unique-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-unique-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。unique()函数**用于沿着张量的一个轴寻找唯一的元素。

**语法:**

```
tf.unique (x, axis?)
```

**参数:**

*   **x:** 它是第一张张量输入，可以是 tf 类型。张量，或类型，或数组。参数可以是这些类型(int32、string、bool)。
*   **轴(**号 **):** 是可选的第二张量输入。张量的轴用于寻找唯一的元素。

**返回值:**返回值和索引。

**示例 1:** 在本例中，我们定义了一个整数类型的输入张量，然后打印它的唯一值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const a = tf.tensor1d([1, 1, 2, 2, 4, 4, 7, 7, 8]);

// Calling unique() method 
const {values, indices} = tf.unique(a);

// Printing the values and indices 
values.print();   // [1, 2, 4, 7, 8,]
indices.print();  // [0, 0, 1, 1, 2, 2, 3, 3, 4]
```

**输出:**

```
Tensor
    [1, 2, 4, 7, 8]
Tensor
    [0, 0, 1, 1, 2, 2, 3, 3, 4]
```

**示例 2:** 在本示例中，使用了轴参数。为了创建输入张量，我们使用 **.tensor2d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements 
const a = tf.tensor2d([[0, 0, 0], [2, 0, 0], [2, 0, 0]]);

// Calling the unique() method 
const {values, indices} = tf.unique(a, 0)

// Printing the values and indices
values.print();   // [[1, 0, 0],
                  //  [2, 0, 0]]
indices.print();  // [0, 0, 1]
```

**输出:**

```
Tensor
    [[0, 0, 0],
     [2, 0, 0]]
Tensor
    [0, 1, 1]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#unique