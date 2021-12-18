# tensorlow . js TF . isinf()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-isinf-function/

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。函数**用于寻找所述张量输入的无穷大或-无穷大元素。

**语法:**

```
tf.isInf(x)
```

**参数:**

*   **x:** 是张量输入，可以是 tf 类型。张量，或类型，或数组。

**返回值:**返回 tf。张量对象。然而，它对于无限元素返回真，对于有限元素返回假。

**示例 1:** 在本例中，我们定义了一个输入张量，然后为无限值打印 true，为有限值打印 false。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([3, .5, -38.8, NaN]);

// Calling isInf() method and
// printing output
y.isInf().print();
```

**输出:**

```
Tensor
    [false, false, false, false]
```

**示例 2:** 在本例中，参数直接传递给函数的 *isInf。*

## *Javascript*

```
*// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining tensor input
var val = [Infinity, -Infinity, 5.78799797];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling isInf() method
var res = tf.isInf(y)

// printing output
res.print();*
```

**输出:**

```
Tensor
    [true, true, false]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#isInf