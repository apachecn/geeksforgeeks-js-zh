# Tensorflow.js tf.fill()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-fill-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-fill-function/)

**Tensorflow.js** 是一个**开源库**，用于在 Javascript 中创建**机器学习**模型，允许用户直接在**浏览器**中运行模型。

**tf.fill()** 是在类 **tf 中定义的函数。张量**。它用于创建一个充满**标量值**的张量。

**语法:**

```
tf.fill( shape, value, dtype )
```

**参数:**

*   **形状:**这是一个**整数数组**，定义了**输出张量**的**形状**。
*   **值:**这是一个**标量值**，**输出张量**将被**填充。**
*   **数据类型:**定义**输出张量**中元素的**数据类型**。可以是**' float 32 ' | ' int 32 ' | ' bool ' | ' complex 64 ' | ' string '**。包含**可选**，**默认**值为**“浮动 32”。**

**返回值:**返回用**标量值**填充的**指定形状**的**张量**。

**示例 1:用标量数字**

*   Fill in tensor to create shape tensor **[4,2]** Fill in **Scalar value 2** .
*   Set **default data type** of the element in the output tensor as **floating** .

## Javascript

```
// Dynamic loading the "@tensorflow/tfjs" module
const tf = require('@tensorflow/tfjs');
require('@tensorflow/tfjs-node');

// Creating a tensor of of shape [4,2] filled with 
// scalar value 2
var matrix = tf.fill(shape = [4,2],value = 2)

// Printing the tensor
matrix.print()
```

**输出:**

```
Tensor
    [[2, 2],
     [2, 2],
     [2, 2],
     [2, 2]]
```

**示例 2:明确定义元素的数据类型**

*   Create a shape tensor **[3,4]** and fill **the string' gfg'.**

## Javascript

```
// Dynamic loading the "@tensorflow/tfjs" module
const tf = require('@tensorflow/tfjs');
require('@tensorflow/tfjs-node');

// Creating a tensor  of shape [3,4] filled
// with string value 'Gfg'
var matrix = tf.fill(shape = [3, 4], 
        value = 'Gfg', dtype = 'string')

// Printing the tensor
matrix.print()
```

**输出:**

```
Tensor
    [['Gfg', 'Gfg', 'Gfg', 'Gfg'],
     ['Gfg', 'Gfg', 'Gfg', 'Gfg'],
     ['Gfg', 'Gfg', 'Gfg', 'Gfg']]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#fill