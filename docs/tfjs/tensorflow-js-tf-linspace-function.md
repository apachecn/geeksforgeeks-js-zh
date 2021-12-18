# tensorlow . js TF . linspace()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-linspace-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。linspace()函数**用于在规定的时间间隔内找到一系列规则间隔的数字。

**语法:**

```
tf.linspace(start, stop, num)
```

**参数:**

*   **开始:**是要生成的系列的规定开始值，类型号。
*   **stop:** 是要生成的系列的规定结束值，类型号。
*   **编号:**是要生成的值的规定数量，并且是类型号。

**返回值:**返回 tf。张量 1D 对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining all the parameters
var strt = 3;
var stp = 20;
var num = 5;

// Calling linspace() method and
// Printing output
tf.linspace(strt, stp, num).print();
```

**输出:**

```
Tensor
    [3, 7.25, 11.5, 15.75, 20]
```

**示例 2:** 对所有规定的参数使用浮点值。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling linspace() method and
// Printing output
tf.linspace(12.4, 29.7, 5.4).print();
```

**输出:**

```
Tensor
    [12.3999996, 16.3318176, 20.2636356, 24.1954536, 28.1272717]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#linspace