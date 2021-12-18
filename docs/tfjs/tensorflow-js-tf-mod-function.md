# tensorlow . js TF . mod()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-mod-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.mod()函数**返回元素方式的除法余数。

**操作:**楼层(x / y) * y + mod(x，y) = x。

**注意:**支持广播。

**语法:**

```
tf.mod(x, y).
```

**参数:**这个函数接受三个参数，如下图所示:

*   **X:** It is a tensor.
*   **Y:** It is a tensor. It must be of the same type as x.

**返回值:**一张张量。与 x 的类型相同。

**例 1:** 我们还公开了 **tf.mod()** 与本次操作签名相同，断言 a 和 b 形状相同(不广播)。

## Javascript

```
// Importting the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor
const x = tf.tensor([9, 12, 3, 20, 7]);
const y = tf.tensor([2, 2, 9, 4, 2]);

tf.mod(x,y).print();
```

**输出:**

```
Tensor
    [1, 0, 3, 0, 1]
```

**示例 2:** 在运算中组合数组和标量值时最简单的广播示例:

## Javascript

```
// Importing the tensorflow library
import * as tf from "@tensorflow/tfjs"

// Broadcast a mod b.
const x = tf.tensor([2, 4, 5, 8]);
const y = tf.scalar(5);

x.mod(y).print();
```

**输出:**

```
Tensor
    [2, 4, 0, 3]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#mod