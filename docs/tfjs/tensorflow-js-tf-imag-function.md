# tensorlow . js TF . imag()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-imag-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。imag()函数**用于寻找所述复数的虚部或实张量输入。此外，如果所述张量输入是实的，则不存在虚部，因此全零张量作为输出返回。

**语法:**

```
tf.imag(input)
```

**参数:**

*   **输入:**是陈述的张量输入，可以是 tf 类型。张量、类型或数组。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.complex([-21, 30], [14, 5]);

// Calling imag() method and
// Printing output
tf.imag(y).print();
```

**输出:**

```
Tensor
    [14, 5]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling imag() method and
// Printing output
tf.imag(tf.complex([-2.1, 3.0], [1.65, 57.5])).print();
```

**输出:**

```
Tensor
    [1.65, 57.5]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#imag