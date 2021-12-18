# Tensorflow.js tf.eye()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-eye-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-eye-function/)

**Tensorflow.js** 是一个用 Javascript 创建机器学习模型的开源库，允许用户直接在浏览器中运行模型。

**tf.eye()** 是在类 tf **中定义的函数。**张量。它用于创建指定行和列的标识矩阵。

形状【m，n】**的**单位矩阵**由所有对角元素的值 1 和剩余位置的值 0 组成。**

****语法:****

```
tf.eye(numRows, numColumns, batchShape, dtype)
```

****参数:****

***   **numrows:** Returns the rows of the identity matrix.*   **numcolumns** : Returns the number of columns in the identity matrix. This is an optional parameter. If not specified, the shape of the returned identity matrix is [numRows, numRows].*   **batchshape:** This is an array , which defines the shape to be attached to the beginning of the shape of the returned identity matrix by copying identity matrix by . This is an optional parameter of . Assuming **batchshape = [a, b], the returned identity matrix is [a, b, numRows, numColumns]***   **[T0】 dtype: 【T1] is specified as the data type that returns the elements in the identity matrix. This is optional for **and** .****

******返回值:**返回一个**张量的单位矩阵。******

******示例 1:** 创建**方形形状******

*****   The **identity matrix** of creates the identity matrix of the shape [3,3] **by defining numrows = 3 in the **TF.eye ()** method.******

## **Javascript**

```
// Dynamic loading the "@tensorflow/tfjs" module
const tf = require('@tensorflow/tfjs');
require('@tensorflow/tfjs-node');

// Creating an identity matrix  of shape [3,3]
var matrix = tf.eye(numRows = 3)

// Printing the identity matrix
matrix.print()
```

****输出:****

```
Tensor
    [[1, 0, 0],
     [0, 1, 0],
     [0, 0, 1]]
```

****示例 2:** 创建矩形形状的身份矩阵**

***   By defining numrows = 3 and numcolumns = 4 in the **TF. Eye ()** method, the identity matrix of the shape **[3,4] is created.****

## ****Javascript****

```
**// Dynamic loading the "@tensorflow/tfjs" module
const tf = require('@tensorflow/tfjs');
require('@tensorflow/tfjs-node');

// Creating an identity matrix  of shape [3,4]
var matrix = tf.eye(numRows = 3, numColumns = 4)

// Printing the identity matrix
matrix.print()**
```

******输出:******

```
**Tensor
    [[1, 0, 0, 0],
     [0, 1, 0, 0],
     [0, 0, 1, 0]]**
```

******示例 3:** 通过指定 **batchShape******

*****   Create **Identity Matrix Create the identity matrix **[2,3]** of the shape by defining **numrows = 2** and **numcolumns = 3** in **TF.eye ()** method.***   **跩乎**分批形状=【3】*****   Copying the above-mentioned identity matrix **for** three times returns that the shape of the identity matrix **is **[3,2,3]********

## **Javascript**

****输出:****

```
Tensor
    [[[1, 0, 0],
      [0, 1, 0]],

     [[1, 0, 0],
      [0, 1, 0]],

     [[1, 0, 0],
      [0, 1, 0]]]
```

****参考:**T2】https://js.tensorflow.org/api/latest/#eye**