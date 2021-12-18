# tensorlow . js TF . dispose()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-dispose-function/

Tensorflow.js 是 Google brain 团队开发的开源库，用于在浏览器或节点环境中运行深度学习神经网络。

**。dispose()** 函数用于向内存中分配一个张量。

**语法:**

```
tensor.dispose()
```

**参数:**该方法没有任何参数

**返回值:**无效

**示例 1:** 在本例中，我们将使用 tf.dispose 函数来处理张量。

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor
var tr = tf.tensor([1, 2, 3, 4, 5, 6, 7]);

// Disposing the tensor
tr.dispose()

// Trying to print it now
tr.print()
```

**输出:**

```
An error occurred 
  Tensor is disposed
```

**示例 2:** 在本例中，我们将创建一个秩为 2 的张量，并尝试使用 tf.dispose 函数打印到前后。

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Create a new tensor
var tr2d = tf.tensor2d([1, 2, 3, 4], [2, 2]);

// Print the tensor
tr2d.print()

// Dispose the tensor
tr2d.dispose()

// Try to print it again
tr2d.print()
```

**输出:**

```
"Tensor
    [[1, 2],
     [3, 4]]" 
```

**示例 3:** 在本例中，我们创建了一个包含值、形状和数据类型的张量。然后，我们将使用 tf.dispose()函数对其进行处置:

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Creating a value variable which
// stores the value
var value = ['1', '2', '3', '4', '5', '6']

// Creating a shape variable
// which stores the shape
var shape = [2, 3]

// Creating a d_Type variable
// which stores the data-type
var d_Type = 'string'

// Creating the tensor
var tr3d = tf.tensor(value, shape, d_Type)

// Printing the tensor
tr3d.print()
```

**输出:**

```
"Tensor
    [['1', '2', '3'],
     ['4', '5', '6']]" 
```

**参考:**T2】https://js.tensorflow.org/api/latest/#dispose