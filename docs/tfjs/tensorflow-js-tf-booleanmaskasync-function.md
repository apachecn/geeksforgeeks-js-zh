# tensorlow . js TF . boolean man sync()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-boolean man sync-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。booleanMaskAsync()函数**用于实现对所述输入张量的布尔屏蔽。

**语法:**

```
tf.booleanMaskAsync(tensor, mask, axis?)
```

**参数:**

*   **张量:**是所述的 N-D 张量，可以是 tf 型。张量、类型或数组。
*   **遮罩:**是所述的 K-D 布尔张量。其中，K < = N 加 K 应该是不主动识别的。它可以是 tf 类型。张量、类型或数组。
*   **轴:**它是类型号的可选参数。它是一个 0-D 整数型张量，表示所述张量中要屏蔽的轴。这里，默认的值是从第一个大小屏蔽的零，否则(K +轴< = N)。

**返回值:**返回 Promise(tf。张量)。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input and mask
const tn = tf.tensor2d(
    [7, 8, 9, 10, 11, 12, 5, 62], [4, 2]);
const msk = tf.tensor1d([2, 1, 2, 3], 'bool');

// Calling tf.booleanMaskAsync() method and
// Printing output
const res = await tf.booleanMaskAsync(tn, msk);
res.print();
```

**输出:**

```
Tensor
    [[7 , 8 ],
     [9 , 10],
     [11, 12],
     [5 , 62]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling tf.booleanMaskAsync() method and
// Printing output
const res = await tf.booleanMaskAsync(
    tf.tensor2d([34, 17, 7, 8], [2, 2]), 
    tf.tensor1d([1, 1], 'bool'), 1);

res.print();
```

**输出:**

```
Tensor
    [[34, 17],
     [7 , 8 ]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#booleanMaskAsync