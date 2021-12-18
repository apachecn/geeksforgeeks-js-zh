# tensorflow . js TF . layers . masking()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-masking-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-masking-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf.layers.masking()** 函数用于通过使用掩码值来屏蔽序列，从而跳过时间步长。

**语法:**

```
tf.layers.masking(arguments)
```

**参数**

*   **输入形状:**是一个可选参数，用于创建输入图层，取数值如 number 和 null。
*   **batchInputShape :** 是一个可选参数，用于在主图层之前创建输入图层，取 number、null 等值。
*   **batchSize :** Its 是一个可选参数，用于制作 batchInputShape、和，它只接受数字。
*   **dtype :** 为可选参数，代表数据类型。默认情况下，它有“float32”，还支持其他值，如“int32”、“bool”等。
*   **名称:**为可选参数，用于定义图层名称，接受字符串。
*   **可训练**:是一个可选参数，决定提供的输入图层是否更新。它接受布尔值。
*   **权重:**拥有图层的起始权重。它也是一个可选参数。
*   **输入类型:**是用于输入数据类型的可选参数。像 dtype 一样，它也支持它的所有值。

**返回值:**返回屏蔽。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing the 1d tensor
const geek= tf.tensor1d([1, 2, 3, 4]);

// Reshaping tensor
const geek1 = tf.reshape(geek,[2,2]);

// Creating masking object of poolSize 2*2
const mask = tf.layers.masking({poolSize:[2,2]});

// Applying masking on img1 tensor
const result=mask.apply(geek1);

// Printing the result tensor
result.print();
```

**输出:**

```
Tensor
    [[1, 2],
     [3, 4]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Reshaping tensor
const geek1 = tf.reshape(tf.tensor1d([5, 6, 7, 8]),[2,2]);

// Applying masking on geek1 tensor
tf.layers.masking(
  {
    poolSize:[2,2]
  }
).apply(
  geek1).print();
```

**输出:**

```
Tensor
    [[5, 6],
     [7, 8]]
```

**参考:**T2】https://js.tensorflow.org/api/3.6.0/#layers.masking