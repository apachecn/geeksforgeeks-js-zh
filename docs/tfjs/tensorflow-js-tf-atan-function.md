# tensorlow . js TF . atan()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-atan-function/

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。atan()函数**用于找到所述张量输入的 *atan* ，并按元素方式完成。

**语法:**

```
tf.atan(x)
```

**参数:**

*   **x:** 是要计算其 *atan* 值的张量输入，可以是 *tf 类型。张量*，或*型达瑞*，或*阵列*。

**返回值:**返回 *tf。张量*对象。

**示例 1:** 在本例中，我们定义了一个整数类型的输入张量，然后打印其*和*值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([9, 10, 11, 12]);

// Calling atan() method and
// Printing output
y.atan().print();
```

**输出:**

```
Tensor
    [1.4601501, 1.4711384, 1.4801465, 1.4876647]
```

**示例 2:** 在本例中，浮点类型值被视为张量输入，参数直接传递给 *atan* 函数。

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [.5, 4.9, .275];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling atan() method
var res = tf.atan(y)

// Printing output
res.print();
```

**输出:**

```
Tensor
    [0.4636506, 1.369487, 0.2683674]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#atan