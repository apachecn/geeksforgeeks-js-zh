# tensorlow . js TF . atanh()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-atanh-function/

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

那个。 **atanh()函数**用于找到所述张量输入的反双曲 *tan* ，并按元素进行。

**语法:**

```
tf.atanh(x)
```

**参数:**

*   **x:** 是张量输入，其 *atanh* 值将被计算，并且它可以是类型 *tf。张量*，或*型达瑞*，或*阵列*。

**返回值:**返回 *tf。张量*对象。

**示例 1:** 在本例中，我们定义了一个整数类型的输入张量，然后打印其*和*值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([1, 15, 38, 0]);

// Calling atanh() method and
// Printing output
y.atanh().print();
```

**输出:**

```
Tensor
    [Infinity, NaN, NaN, 0]
```

**示例 2:** 在本例中，浮点类型值被视为张量输入，参数直接传递给 *atanh* 函数。

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [0.5, 1.5, .66];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling atanh() method
var res = tf.atanh(y)

// Printing output
res.print();
```

**输出:**

```
Tensor
    [0.5493062, NaN, 0.7928137]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#atanh