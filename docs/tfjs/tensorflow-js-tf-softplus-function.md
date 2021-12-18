# tensorlow . js TF . soft plus()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-soft plus-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。softplus()函数**用于查找所述输入张量的 softplus，即 ***log(exp(x) + 1)*** ，并按元素进行。

**语法:**

```
tf.softplus(x)
```

**参数:**

*   **x:** 是陈述的张量输入，可以是 tf 类型。张量、类型或数组。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([11, 17, 0, NaN, -41]);

// Calling softplus() method and
// Printing output
y.softplus().print();
```

**输出:**

```
Tensor
    [11.0000162, 17, 0.6931472, NaN, 0]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining tensor input
var val = [1.5, .4, .23, null, 'a'];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling softplus() method
var res = tf.softplus(y)

// Printing output
res.print();
```

**输出:**

```
Tensor
    [1.7014132, 0.9130152, 0.8147451, 0.6931472, NaN]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#softplus