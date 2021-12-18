# tensorlow . js TF . scarned()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-scattered-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。散射和()函数**用于通过根据所述索引利用对所述形状张量的零张量内的各个切片或值的散射更新来形成不同的张量。此外，这个函数是 tf.gatherND()函数的否定，该函数从一个声明的张量中获取切片或值。

**语法:**

```
tf.scatterND(indices, updates, shape)
```

**参数:**

*   **指数:**是所述张量保持朝向输出张量的指数，并且它可以是 tf 类型。张量、类型或数组。
*   **更新:**保持指数值的是所述张量，它可以是 tf 类型。张量、类型或数组。
*   **形状:**是输出张量的规定形状，类型号为[]。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining indices, updates and shape
const ind = tf.tensor2d([6, 5, 2], [3, 1], 'int32');
const updat = tf.tensor1d([1, 2, 3]);
const shp = [6];

// Calling tf.scatterND() method and
// Printing output
tf.scatterND(ind, updat, shp).print();
```

**输出:**

```
Tensor
    [0, 0, 3, 0, 0, 2]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling tf.scatterND() method and
// Printing output
tf.scatterND(tf.tensor2d([5.4, 2.4], [2, 1], 'int32'), 
            tf.tensor1d([1.8, 4.2]), 
            [4]).print();
```

**输出:**

```
Tensor
    [0, 0, 4.1999998, 0]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#scatterND