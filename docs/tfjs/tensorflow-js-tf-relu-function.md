# tensorlow . js TF . rel()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-rel-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。relu()函数**用于寻找所述张量输入的校正线性，即 max(x，0)，并按元素方式进行。

**语法:**

```
tf.relu(x)
```

**参数:**

*   **x:** 是陈述的张量输入，可以是 tf 类型。张量、类型或数组。此外，如果所述数据类型是布尔类型，那么输出数据类型将是类型 *int32。*

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([11, 76, 0, -4, 6]);

// Calling relu() method and
// Printing output
y.relu().print();
```

**输出:**

```
Tensor
    [11, 76, 0, 0, 6]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining tensor input
var val = [1.5, -5, .22, null, 'a'];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling relu() method
var res = tf.relu(y)

// Printing output
res.print();
```

**输出:**

```
Tensor
    [1.5, 0, 0.22, 0, NaN]
```

**参考资料:**[https://js . tensorlow . org/API/latest/# rel](https://js.tensorflow.org/api/latest/#relu)