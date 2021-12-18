# tensorlow . js TF . value andgrad()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-valueandgrad-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.valueAndGrad()** 函数用于返回指定函数 f(x)相对于 x 的梯度以及 f()的值。

**语法:**

```
tf.valueAndGrad (f)
```

**参数:**该函数接受如下所示的参数:

*   **f:** 正在计算梯度的指定函数 f(x)。

**返回值:**返回指定函数 f(x)相对于 x 的梯度以及 f()的值。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a function f(x) = x^2
const f = x => x.square();

// Calling the .valueAndGrad() function over
// the above function as its parameter which
// calculates f'(x) = 2x
const g = tf.valueAndGrad(f);

// Initializing a Tensor of values at which
// value of gradient is calculated
const x = tf.tensor1d([0, 1, 2, 3]);

// Returning the value of f() and 
// gradient of f(x)
const {value, grad} = g(x);

// Getting the value of f()
console.log('value');
value.print();

// Getting the gradient of f(x) at 
// the above tensor values
console.log('grad');
grad.print();
```

**输出:**

```
value
Tensor
   [0, 1, 4, 9]
grad
Tensor
   [0, 2, 4, 6]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using a function f(x) = x^3 as the parameter
// for the .valueAndGrad() function which
// calculates f'(x) = 3x^2
const g = tf.valueAndGrad(x => x.pow(tf.scalar(3, 'int32')));

// Using a Tensor of values at which
// value of gradient is calculated 
const {value, grad} = g(tf.tensor1d([-1, 0, 0.3, 4]));

// Getting the value of f()
console.log('value');
value.print();

// Getting the gradient of f(x)
console.log('grad');
grad.print();
```

**输出:**

```
value
Tensor
   [-1, 0, 0.027, 64]
grad
Tensor
   [3, 0, 0.27, 48]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#valueAndGrad