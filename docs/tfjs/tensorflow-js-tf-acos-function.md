# tensorlow . js TF . acos()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-acos-function/

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。acos()函数**用于查找所述张量元素输入的 *acos* 。

**语法:**

```
tf.acos(x)
```

**参数:**

*   **x:** 是张量输入元素，其 *acos* 值将被计算。

**返回值:**返回 *tf。张量*对象。

**示例 1:** 在这个示例中，我们定义了一个整数类型的输入张量，然后打印它的 acos 值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([1, 4, 0, 11]);

// Calling acos() method and
// Printing output
y.acos().print();
```

**输出:**

```
Tensor
    [0, NaN, 1.5707288, NaN]
```

**示例 2:** 在本例中，浮点类型值被视为张量输入，参数直接传递给 *acos* 函数。

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [.5, .4, .2];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling acos() method
var res = tf.acos(y)

// Printing output
res.print();
```

**输出:**

```
Tensor
    [1.0471513, 1.1592351, 1.3694812]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#acos