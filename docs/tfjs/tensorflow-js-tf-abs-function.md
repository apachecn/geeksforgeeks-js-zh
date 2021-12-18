# Tensorflow.js tf.abs()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-ABS-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-abs-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。abs()函数**用于求所述元素的绝对值。

**语法:**

```
tf.abs (x)
```

**参数:**

*   **x:** 是要计算绝对值的张量输入元素。

**返回值:**返回给定元素的绝对值。

**示例 1:** 在这个示例中，我们定义了一个整数类型的输入张量，然后打印它的绝对值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Defining tensor input elements
const y = tf.tensor1d([-7, 8, -9, 13]);

// Calling abs() method and
// printing the output
y.abs().print();
```

**输出:**

```
Tensor
    [7, 8, 9, 13]
```

**示例 2:** 在本例中，浮点类型值被视为张量输入，参数直接传递给 abs 函数。

## Javascript

```
// Defining tensor input elements
const z = tf.tensor1d([-3.91, 5.73]);

// Calling abs() method and directly
// passing tensor inputs
res = tf.abs(z);

// Prints output
res.print();
```

**输出:**

```
Tensor
    [3.9100001, 5.73]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#abs