# tensorlow . js TF . available()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-available-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。disposeVariables()函数**用于处理存储在后端引擎中的每个变量。

**语法:**

```
tf.disposeVariables()
```

**参数:**此方法不接受任何参数。

**返回值:**返回 void。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Declaring a variable
var x = tf.tensor([1, 2, 3, 4]);

// Calling disposeVariables() method
tf.disposeVariables();

// Printing output
console.log("Variables disposed.")
```

**输出:**

```
Variables disposed.
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Declaring two tensors
var t1 = tf.tensor([1.1, 2.1, 3.1]);
var t2 = tf.tensor([null, 0, -2]);

// Calling dispose() and disposeVariables()
// method
tf.dispose(t2);
tf.disposeVariables();

// Printing outputs
console.log(t1);
console.log(t2);
```

**输出:**

```
Tensor
    [1.1, 2.0999999, 3.0999999]

An error occured on line: 15
Tensor is disposed.
```

这里，张量 t2 的处理出现了错误。

**参考:**T2】https://js.tensorflow.org/api/latest/#disposeVariables