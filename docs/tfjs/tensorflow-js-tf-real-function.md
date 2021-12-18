# Tensorflow.js tf.real()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-real-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-real-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。real()函数**用于为所述张量输入找到张量，该张量为 float 类型，是输入中被视为复数的每个元素的实部。

**语法:**

```
tf.real( input )
```

**参数:**

*   **输入:**是张量*输入，*以复数为输入。

**返回值:**返回复数或实张量输入的实部。

**示例 1:** 在本例中，我们定义了一个 float 类型的输入张量，然后打印它的实部。为了创建输入张量，我们使用了。 **complex()** 方法，为了打印输出，我们使用了**。print()** 方法。

## Javascript

```
// Defining input tensor
const y = tf.complex([-9.25, 12.25], [6.66, 8.66]);

// Calling real() function and
// printing the output
tf.real(y).print();
```

**输出:**

```
Tensor
    [-9.25, 12.25]
```

**示例 2:** 在本例中，我们使用 *null、*字符以及整型值作为张量输入。

## Javascript

```
// Defining input tensor
const y = tf.complex([null, 'a'], [5, 'r']);

// Calling real() function
var z = tf.real(y);

// Prints output
z.print();
```

**输出:**

```
Tensor
    [0, NaN]
```

在上例中，空值返回*零*，字符类型值返回 *NaN。*

**参考:**T2】https://js.tensorflow.org/api/latest/#real