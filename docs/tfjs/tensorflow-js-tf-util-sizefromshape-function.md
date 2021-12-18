# tensorlow . js TF . util . sizeefromhape()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-util-sizeefromhape-function/

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**util . SizeFromShape()函数**用于从所述形状中找到元素的数量，即所述张量输入的大小。

**语法:**

```
tf.util.sizeFromShape(shape)
```

**参数:**

*   **形状:**是要返回大小的指定形状。它是编号为[]的类型。

**返回值:**返回一个数字。

**例 1:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining shape
const sh = [5, 8, 1];

// Calling tf.util.sizeFromShape() method
const num = tf.util.sizeFromShape(sh);

// printing output
console.log(num);
```

**输出:**

```
40
```

**例 2:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling tf.util.sizeFromShape() method and
// printing output
console.log(tf.util.sizeFromShape([1.4, 5.6, 9.0]));
```

**输出:**

```
70.55999999999999
```

**参考资料:**[https://js . tensorlow . org/API/1 . 0 . 0/# sizeefromhape](https://js.tensorflow.org/api/1.0.0/#sizeFromShape)