# tensorlow . js TF . value andgrad()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-value and grads-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-valueandgrads-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。valueAndGrads()函数**相当于 tf.grads()方法，但也返回 f()的度量。它在 f()返回您需要演示的近似值时有效。

**注意:**这里的输出是一个富裕的对象，具有以下特征:

*   **Gradient:** It is the gradient of f () relative to each input, that is, the output of grads () method.
*   **value:** is the value restored by f(x).

**语法:**

```
tf.valueAndGrads(f)
```

**参数:**

*   **f:** It is the specified function f(x) for which the slope is to be calculated. Its type is (…args: tf. Tensor []) = > TF. Tensor.

**返回值:**返回梯度和值(即 args: tf。张量[]，dy？:tf。张量)= > {梯度:tf。张量[]；值:tf。张量；}.

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining function
const fn = (x, y) => x.add(y);

// Calling valueAndGrads() method
const gr = tf.valueAndGrads(fn);

// Defining tf.tensor1d inputs
const x = tf.tensor1d([66, 51]);
const y = tf.tensor1d([-21, -13]);

// Defining value and grads
const {value, grads} = gr([x, y]);
const [dx, dy] = grads;

// Printing value
console.log('val');
value.print();

// Printing gradients
console.log('dx');
dx.print();
console.log('dy');
dy.print();
```

**输出:**

```
val
Tensor
    [45, 38]
dx
Tensor
    [1, 1]
dy
Tensor
    [1, 1]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling valueAndGrads() method
// with its parameter
const gr = tf.valueAndGrads((x, y) => x.div(y));

// Defining tf.tensor1d inputs of
// floating point numbers
const x = tf.tensor1d([4.7, 5.8, 99.7]);
const y = tf.tensor1d([9.5, -20.5, null]);

// Defining value and grads
const {value, grads} = gr([x, y]);
const [dx, dy] = grads;

// Printing value
console.log('val');
value.print();

// Printing gradients
console.log('dx');
dx.print();
console.log('dy');
dy.print();
```

**输出:**

```
val
Tensor
    [0.4947368, -0.2829268, Infinity]
dx
Tensor
    [0.1052632, -0.0487805, Infinity]
dy
Tensor
    [-0.0520776, -0.0138013, -Infinity]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#valueAndGrads