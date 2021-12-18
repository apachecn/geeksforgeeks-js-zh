# tensorlow . js TF . rel 6()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-rel 6-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**.relu6()函数**用于求整流后的线性 6，即最小值(最大值(x，0)，6)，并按元素进行。

**语法:**

```
tf.relu6(x)
```

**参数:**

*   **x:** 是陈述的张量输入，可以是 tf 类型。张量、类型或数组。此外，如果所述数据类型是*布尔*类型，那么输出数据类型将是 int32 类型。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([1, 176, 0, NaN, -4]);

// Calling relu6() method and
// Printing output
y.relu6().print();
```

**输出:**

```
Tensor
    [1, 6, 0, NaN, 0]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining tensor input
var val = [9.5, .4, "abc", null, 'z'];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling relu6() method
var res = tf.relu6(y)

// Printing output
res.print();
```

**输出:**

```
Tensor
    [6, 0.4, NaN, 0, NaN]
```

**参考资料:**[https://js . tensorlow . org/API/latest/# rel 6](https://js.tensorflow.org/api/latest/#relu6)