# Tensorflow.js tf.tensor6d()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-tensor6d-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor6d-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**.tensor6d()函数**用于创建一个新的 **6 维**张量，其参数包括值、形状和数据类型。

#### 语法:

```
tf.tensor6d(value, shape?, dataType?)
```

#### 参数:

*   **值**:张量的值，可以是数字的**嵌套数组**，或者是**平面数组**，或者是**类型的数组**。
*   **形状**:取张量的形状。如果没有提供，张量将从**值**推断其**形状**。这是一个可选参数。
*   **数据类型**:可以是“ **float32** 或“ **int32** 或“ **bool** 或“ **complex64** 或“ **string** ”值。这是一个可选参数。

**返回值:**返回相同数据类型的张量。返回的张量将永远是 6 维的。

**注**:6d 张量功能也可以使用 tf.tensor()函数实现，但是使用 tf.tensor6d()可以使代码易于理解和阅读。

**示例 1:** 这里，我们正在创建 6d 张量并打印它。为了创建 6d 张量，我们使用。 **tensor6d** ()功能，和我们用的一样。函数打印张量。这里，我们将把 6d 数组(即嵌套数组)传递给 value 参数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs";

// Create the tensor
var example1 = tf.tensor6d([[[[
    [[1, 3], [2, 8]],
    [[3, 9], [4, 2]]
]]]]);

// Print the tensor
example1.print()
```

**输出:**

```
Tensor
    [[[[[[1, 3],
         [2, 8]],

        [[3, 9],
         [4, 2]]]]]]

```

**示例 2:** 在这个示例中，我们正在创建张量，在这里我们传递平面数组并指定张量的形状参数。我们将在这里看到形状参数的用法。

## Javascript

```
// Import the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Define the value of the tensor
var value = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12];

// Specify the shape of the tensor
var shape = [1, 2, 6, 1, 1, 1];

// Create the tensor
var example2 = tf.tensor6d(value, shape);

// Print the tensor
example2.print();
```

**输出:**

```
Tensor
    [[[ [ [[1 ],]],
        [ [[2 ],]],
        [ [[3 ],]],
        [ [[4 ],]],
        [ [[5 ],]],
        [ [[6 ],]]],

      [ [ [[7 ],]],
        [ [[8 ],]],
        [ [[9 ],]],
        [ [[10],]],
        [ [[11],]],
        [ [[12],]]]]]

```

**示例 3:** 在本例中，我们将通过指定值、形状和数据类型来创建张量。我们将创建张量，其中所有值都是字符串数据类型。

## Javascript

```
// Import the tensorflow.js library
import * as tf from "@tensorflow/tfjs";

// Define the value of the tensor
var value = ["C", "C++", "Java", "Python",
            "PHP", "JS", "SQL", "React"];

// Specify the shape of the tensor
var shape = [1, 2, 4, 1, 1, 1];

// Create the tensor
var example3 = tf.tensor6d(value, shape);

// Print the tensor
example3.print();
```

**输出:**

```
Tensor
    [[[ [ [['C'     ],]],
        [ [['C++'   ],]],
        [ [['Java'  ],]],
        [ [['Python'],]]],

      [ [ [['PHP'   ],]],
        [ [['JS'    ],]],
        [ [['SQL'   ],]],
        [ [['React' ],]]]]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#tensor6d