# Tensorflow.js tf.variable()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-variable-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-variable-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它帮助开发人员在 JavaScript 中开发 ML 模型，并直接在浏览器或 Node.js 中使用 ML。

**tf.variable()函数**用于用提供的初始值创建一个新变量。

**语法:**

```
tf.variable(initialValue, trainable, name, dtype)
```

**参数:**

*   **initialValue:** 新变量将从中初始化的张量的初始值。
*   **可训练:**为可选参数。如果允许真优化器更新变量，如果不允许假优化器更新变量，则为布尔类型。
*   **名称:**也是可选参数。它是字符串类型。它用于作为唯一标识的变量名称。
*   **数据类型:**也是可选参数。如果它作为参数传递，intialValue 将被更改为指定的数据类型。

**返回值:**此函数返回 tf.variable。

**例 1:**

## Javascript

```
// Creating and initializing a new variable
var val = tf.variable(tf.tensor2d(
    [8, 2, 5, 6],
    [2, 2]
));

// Printing the tensor
val.print()
```

**输出:**

```
Tensor
   [[8, 2],
    [5, 6]]
```

**例二:**

## Javascript

```
// Creating and initializing a new variable
var val = tf.variable(tf.tensor([1, 2, 5, 6]));

// Printing the tensor
val.print()
```

**输出:**

```
Tensor
   [1, 2, 5, 6]
```

**例三:**

## Javascript

```
// Creating and initializing a new variable
const x = tf.variable(tf.tensor([1, 2, 3]),
    true,"gfg",'complex64');

// Printing the tensor
x.print();
```

**输出:**

```
Tensor
   [1 + 0j, 2 + 0j, 3 + 0j]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#variable