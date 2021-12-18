# Tensorflow.js tf.tensor2d()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-tensor2d-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor2d-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。 **.tensor2d()函数**用于创建一个新的二维张量，参数为**值**、**形状**和**数据类型**。

**语法:**

```
tf.tensor2d (value, shape, datatype)
```

**参数:**

*   **Value: the value of** tensor, which can be a number **nested array** , or a **planar array** , or a **typed array** .
*   **shape:** takes the shape of a tensor. If not provided, the tensor will infer its **shape** from the **value** . This is an optional parameter.
*   **Data type:** can be **"float 32"** or **"Int32"** or **"Bool"** or **"Complex 64"** or **"String" [T11 This is an optional parameter.**

**返回值:**返回相同数据类型的张量。返回的张量总是二维的。

**注意:**2d 张量功能也可以使用 [**tf.tensor()**](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-function/) 函数来实现，但是使用 **tf.tensor2d()** 可以使代码易于理解和阅读。

**示例 1:** 在这个示例中，我们正在创建一个 2D 张量并打印它。为了创建 2D 张量，我们使用了 **.tensor2d()** 函数，并且使用了**。print()** 功能打印张量。这里，我们将把 2D 数组(即嵌套数组)传递给 value 参数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs";

// Create the tensor
let example1 = tf.tensor2d([ [ 1, 2, 3 ], [ 4, 5, 6 ] ]);

// Print the tensor
example1.print()
```

**输出:**

```
Tensor
    [[1, 2, 3],
     [4, 5, 6]]
```

**示例 2:** 在这个示例中，我们正在创建张量，在这里我们传递平面数组并指定张量的形状参数。我们将在这里看到**形状**参数的用法。

## Javascript

```
// Import the tensorflow.js library
import * as tf from "@tensorflow/tfjs";

// Define the value of the tensor
const value = [1, 2, 3, 4, 5, 6, 7, 8];

// Specify the shape of the tensor
const shape = [2, 4];

// Create the tensor
let example2 = tf.tensor2d(value, shape);

// Print the tensor
example2.print();
```

**输出:**

```
Tensor
    [[1, 2, 3, 4],
     [5, 6, 7, 8]]
```

在上面的例子中，我们创建了一个 2×4 维的张量。

**示例 3:** 在本例中，我们将通过指定**值**、**形状**和**数据类型**来创建张量。我们将创建张量，其中所有值都是**字符串**数据类型。

## Javascript

```
// Import the tensorflow.js library
import * as tf from "@tensorflow/tfjs";

// Define the value of the tensor
const value = ["C", "C++", "Java", "Python",
               "PHP", "JS", "SQL", "React"];

// Specify the shape of the tensor
const shape = [2, 4];

// Specify the datatype of value of the tensor
const datatype = "string";

// Create the tensor
let example3 = tf.tensor2d(value, shape, datatype);

// Print the tensor
example3.print();
```

**输出:**

```
Tensor
    [['C'  , 'C++', 'Java', 'Python'],
     ['PHP', 'JS' , 'SQL' , 'React' ]]
```

在上面的例子中，张量的打印值属于*字符串*数据类型。

**参考:**T2】https://js.tensorflow.org/api/latest/#tensor2d