# tensorlow . js TF . grad()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-grad-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-grad-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.grad()** 函数用于返回指定函数 f(x)相对于 x 的梯度。

**语法:**

```
tf.grad (f)
```

**参数:**该函数接受如下所示的参数:

*   **f:** 正在计算梯度的指定函数 f(x)。

**返回值:**返回指定函数 f(x)相对于 x 的梯度。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a function f(x) = x^2
const f = x => x.square();

// Calling the .grad() function which 
// calculates f'(x) and gives value as 2x
const g = tf.grad(f);

// Initializing a tensor of values for
// which gradient will be returned
const x = tf.tensor1d([1, 2, 3]);

// Getting the values of gradient of the
// function f(x) for the above specified
// tensor 
g(x).print();
```

**输出:**

```
Tensor
   [2, 4, 6]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using the function f(x) = x^3 as the 
// parameter for the .grad() function which 
// calculates f'(x) and gives value as 3x^2
const g = tf.grad(x => x.pow(tf.scalar(3, 'int32')));

// Initializing a tensor of values for
// which gradient will be returned
const x = tf.tensor1d([0, 1, 2]);

// Getting the values of gradient of the
// function f(x) for the above specified
// tensor 
g(x).print();
```

**输出:**

```
Tensor
   [0, 3, 12]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#grad