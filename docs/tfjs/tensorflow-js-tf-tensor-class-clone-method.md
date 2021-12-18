# Tensorflow.js tf。张量类。克隆()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-tensor-class-clone-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-class-clone-method/)

**Tensorflow.js** 是一个**开源库**，用于在 **Javascript** 中创建**机器学习模型**，允许用户直接在**浏览器**中运行模型。

**tf.clone()** 是在类 **tf 中定义的函数。张量**。它被用来创建张量的**复制品。**

**语法:**

```
tf.clone( values )
```

**参数:**

*   **值:**它可以是值的张量或值的数组

**返回值:**返回包含与**值**的相同元素的**张量**。

**示例 1:** 输入参数值作为**张量**

## Javascript

```
// Dynamic loading the "@tensorflow/tfjs" module
const tf = require('@tensorflow/tfjs');

//Creating a tensor
var values = tf.tensor([1, 2, 3, 4, 5, 6, 7]);

// Printing the colne of a tensor
tf.clone(values).print()
```

**输出:**

```
Tensor
    [1, 2, 3, 4, 5, 6, 7]
```

**示例 2:** 将参数值输入为值数组

## Javascript

```
// Dynamic loading the "@tensorflow/tfjs" module
const tf = require('@tensorflow/tfjs');

//Creating a tensor
var values = [1, 2, 3, 4, 5, 6, 7];

// Printing the colne of a tensor
tf.clone(values).print()
```

**输出:**

```
Tensor
    [1, 2, 3, 4, 5, 6, 7]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.Tensor.clone