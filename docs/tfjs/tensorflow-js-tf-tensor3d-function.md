# Tensorflow.js tf.tensor3d()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-tensor3d-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor3d-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**.tensor3d()** 函数用于创建一个新的三维张量，其参数为**值**、**形状**和**数据类型**。

**语法:**

```
tf.tensor3d (value, shape, datatype)
```

**参数:**

*   **值:**张量的值，可以是数字的**嵌套数组**，或者是**平面数组**，或者是**类型的数组**。
*   **形状:**取张量的形状。如果没有提供，张量将从**值**推断其**形状**。这是一个可选参数。
*   **数据类型:**可以是**“float 32”**或**“int32”**或**“bool”**或**“complex 64”**或**“string”**值。这是一个可选参数。

**返回值:**返回相同数据类型的张量。返回的张量总是三维的。

**注意:**3d tensor 功能也可以使用 [**tf.tensor()**](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-function/) 功能实现，但是使用 **tf.tensor3d()** 使得代码易于理解和阅读。

**例 1:**

这里，我们正在创建一个 3d 张量并打印它。为了创建三维张量，我们使用 **.tensor3d()** 函数，我们使用**。print()** 功能打印张量。这里，我们将把 3d 数组(即嵌套数组)传递给 value 参数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs";

// Create the tensor
let example1 = tf.tensor3d([
    [
        [1, 2],
        [3, 4],
    ],
    [
        [5, 6],
        [7, 8],
    ],
]);

// Print the tensor
example1.print()
```

**输出:**

```
Tensor        
   [[[1, 2],  
     [3, 4]],

    [[5, 6],  
     [7, 8]]]
```

**例 2:**

这里，在这个例子中，我们正在创建张量，在这里我们传递平面数组并指定张量的形状参数。我们将在这里看到**形状**参数的用法。

## java 描述语言

```
// Import the tensorflow.js library
import * as tf from "@tensorflow/tfjs" 

// Define the value of the tensor
const value = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12];

// Specify the shape of the tensor
const shape = [2, 3, 2];

// Create the tensor
let example2 = tf.tensor3d(value, shape);

// Print the tensor
example2.print();
```

**输出:**

```
Tensor
    [[[1 , 2 ],
      [3 , 4 ],
      [5 , 6 ]],

     [[7 , 8 ],
      [9 , 10],
      [11, 12]]]
```

在上面的例子中，我们创建了一个 2×3×2 维的张量。

**例 3:**

在本例中，我们将通过指定值、形状和数据类型来创建张量。我们将创建张量，其中所有值都是字符串数据类型。

## Javascript

```
// Import the tensorflow.js library
import * as tf from "@tensorflow/tfjs";

// Define the value of the tensor
const value = ["C", "C++", "Java", "Python", 
               "PHP", "JS", "SQL", "React"];

// Specify the shape of the tensor
const shape = [2, 2, 2];

// Create the tensor
let example3 = tf.tensor3d(value, shape);

// Print the tensor
example3.print();
```

**输出:**

```
Tensor
    [[['C'   , 'C++'   ], 
      ['Java', 'Python']],

     [['PHP' , 'JS'    ], 
      ['SQL' , 'React' ]]]
```

在上面的例子中，张量的打印值属于*字符串*数据类型。

**参考:**T2】https://js.tensorflow.org/api/latest/#tensor3d