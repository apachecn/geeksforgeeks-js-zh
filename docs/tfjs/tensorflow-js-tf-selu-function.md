# tensorlow . js TF . selu()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-selu-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。卢瑟()函数**用于寻找成比例的指数线性，并按元素进行。

**语法:**

```
tf.selu(x)
```

其中，x < 0？缩放* alpha *(exp(x)–1):x

**参数:**

*   **X:** is a statement tensor input, which can be of tf type. Tensor, type or array.

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([-1, 76, 0, NaN, -4]);

// Calling selu() method and
// Printing output
y.selu().print();
```

**输出:**

```
Tensor
    [-1.1113307, 79.8532791, 0, NaN, -1.7258986]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining tensor input
var val = [8.5, .14, .22, 'a'];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling selu() method
var res = tf.selu(y)

// Printing output
res.print();
```

**输出:**

```
Tensor
    [8.9309587, 0.1470981, 0.2311542, NaN]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#selu