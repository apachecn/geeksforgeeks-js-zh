# tensorflow . js TF . GaThEnd()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-gathernd-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-gathernd-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**TF . GaThEnd()函数**用于使用输入张量从索引指定的形状中收集切片。

**语法:**

```
tf.gatherND(tensor1, tensor2)
```

**参数:**该函数接受以下两个参数:

*   **张量 1:** 就是我们从中收集值的张量。
*   **张量 2:** 是 K 维整数张量。它充当索引。它必须是 int32 类型。

**返回值:**返回 *tf。张量*对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a 3d tensor as indices.
let geeks = tf.tensor3d([1, 2, 3, 4], [2, 2, 1], 'int32');

// Initializing a 3d tensor as input.
let input = tf.tensor1d([1, 2, 3]);

// Gathering both input and indices.
let answer = tf.gatherND(input, geeks);
answer.print();
```

**输出:**

```
Tensor
    [[2, 3],
     [3, 3]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Gathering the tensor and indices together.
let geeks = tf.gatherND(tf.tensor4d([[[[1], [2]], [[3], [4]]]]),
            tf.tensor2d([1, 1, 1, 0], [2,2], 'int32'));

// Printing the final result.           
geeks.print();
```

**输出:**

```
Tensor
    [[[4],
      [4]],

     [[4],
      [4]]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#gatherND