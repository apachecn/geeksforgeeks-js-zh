# tensorlow . js TF . matmul()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-matmul-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.matMul()** 函数用于计算两个矩阵 A * B 的点积。

**语法:**

```
tf.matMul (a, b, transposeA?, transposeB?)
```

**参数:**该函数接受如下所示的参数:

*   **a:** 这是点积运算中的第一个矩阵。
*   **b:** 这是点积运算中的第二个矩阵。
*   **transpose:**这是可选的，如果设置为真，那么 *a* 在乘法之前被转置。
*   **转置 B:** 这是可选的，如果设置为真，那么 *b* 在乘法之前被转置。

**返回值:**返回两个矩阵的点积。

下面是说明使用 **tf.matMul()** 函数的例子。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a tensor of some elements
let geek1 = tf.tensor2d([2, 1], [1, 2]);
let geek2 = tf.tensor2d([11, 12, 13, 14], [2, 2]);

// Calling the .avgPool3d() function over
// the above tensor as its parameter and 
// printing the result.
geek1.matMul(geek2).print();
```

**输出:**

```
Tensor
     [[35, 38],]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a tensor of some elements
let geek1 = tf.tensor2d([2, 1], [1, 2]);
let geek2 = tf.tensor2d([61, 62, 63, 64], [2, 2]);

// Calling the .avgPool3d() function over
// the above tensor as its parameter and 
// printing the result.
tf.matMul(geek1, geek2).print();
```

**输出:**

```
Tensor
     [[185, 188],]
```

**参考资料:**[https://js . tensorlow . org/API/latest/# matmul](https://js.tensorflow.org/api/latest/#matMul)