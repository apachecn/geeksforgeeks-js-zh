# tensorlow . js TF . expm 1()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-expm 1-function/

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**.expm1()函数**用于求所述张量输入的指数值减一(即 e^x-1)，并且是按元素方式进行的。

**语法:**

```
tf.expm1(x)
```

**参数:**

*   **x:** 是要计算指数值减 1 的张量输入，可以是 tf 类型。张量，或类型，或数组。

**返回值:**返回 tf。张量对象。

**示例 1:** 在本例中，我们定义了一个整数类型的输入张量，然后打印指数值减去 1。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
//import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([5, 1, 8, 0]);

// Calling expm1() method and
// printing output
y.expm1().print();
```

**输出:**

```
Tensor
    [147.4131622, 1.7182819, 2979.9580078, 0]
```

**示例 2:** 在此示例中，浮点类型值被视为张量输入，参数被直接传递给 expm1 函数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [8.6, 0.5, .24];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling expm1() method
var res = tf.expm1(y)

// printing output
res.print();
```

**输出:**

```
Tensor
    [5430.6616211, 0.6487213, 0.2712491]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#expm1