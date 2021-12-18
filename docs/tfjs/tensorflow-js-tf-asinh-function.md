# tensorlow . js TF . asinh()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-asinh-function/

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。asinh()函数**用于找到所述张量输入的反双曲 *sin* ，并按元素进行。

**语法:**

```
tf.asinh(x)
```

**参数:**

*   **x:** 是要计算其 asinh 值的张量输入，可以是 *tf 类型。张量*，或*型达瑞*，或*阵列*。

**返回值:**返回 *tf。张量*对象。

**示例 1:** 在本例中，我们定义了一个整数类型的输入张量，然后将其*作为*值打印出来。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([23, 15, 38, 10]);

// Calling asinh() method and
// Printing output
y.asinh().print();
```

**输出:**

```
Tensor
    [3.8291137, 3.4023068, 4.3309064, 2.9982231]
```

**示例 2:** 在本例中，浮点类型值被视为张量输入，参数直接传递给 *asinh* 函数。

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [1.61, 12.5, 55.34];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling asinh() method
var res = tf.asinh(y)

// Printing output
res.print();
```

**输出:**

```
Tensor
    [1.2542715, 3.2204721, 4.7067246]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#asinh