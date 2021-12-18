# tensorlow . js TF . cum sum()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-cusum-function/

TensorFlow.js 是一个 JavaScript 中的机器学习库。它帮助开发人员在 JavaScript 中开发 ML 模型，并直接在浏览器或 Node.js 中使用 ML。

**tf.cumsum()** 函数用于计算一个 tf 的累计和。沿指定轴的张量。张量的排他累积和的含义是每个张量条目不包括它自己的值，而只包括在排他累积和中沿着指定轴在它之前的值。

**语法:**

```
tf.cumsum(x, axis, exclusive, reverse)
```

**参数:**该方法有四个参数，如上所述，描述如下:

*   **x:** 需要求和的输入张量。它是 tf 类型的。张量、类型或数组。
*   **轴:**我们要求和的轴。这是一个可选参数。默认值为 0。
*   **异或:**决定是否求异或累计和。它是一个布尔值，默认为 false。这是一个可选参数。
*   **反转:**决定是否反方向求和。它是一个布尔值，默认为 false。它也是一个可选参数。

**返回值:**返回一个 tf。张量表示给定张量的累积和。

以下示例演示了 tf.cumsum() 方法。

**例 1:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating and initializing a new variable
const x = tf.tensor([1, 2, 3, 4]);

// Finding the cumulative sum
const a=x.cumsum();

// Printing the tensor
a.print();
```

**输出:**

```
Tensor
   [1, 3, 6, 10]
```

**例 2:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating and initializing a new variable
const x = tf.tensor([1, 2, 3, 4]);

// Finding the cumulative sum
const a=x.cumsum(0,true,true);

// Printing the tensor
a.print();
```

**输出:**

```
Tensor
   [9, 7, 4, 0]
```

**例 3:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating and initializing a new variable
const x = tf.tensor([[1, 2],[3, 4]]);

// Finding the cumulative sum
const a=x.cumsum();

// Printing the tensor
a.print();
```

**输出:**

```
Tensor
   [[1, 2],
    [4, 6]]
```

**例 4:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating and initializing a new variable
const x = tf.tensor([[1, 2],[3, 4]]);

// Finding the cumulative sum
const a=x.cumsum(1);

// Printing the tensor
a.print();
```

**输出:**

```
Tensor
   [[1, 3],
    [3, 7]]
```

**参考:**T2**https://js.tensorflow.org/api/latest/#cumsum**T5】