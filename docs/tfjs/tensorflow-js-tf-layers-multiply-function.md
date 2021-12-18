# tensorflow . js TF . layers . multiply()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-multiple-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-multiply-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**tf.layers.multiply()** 函数用于执行输入数组的逐元素乘法。

**语法:**

```
tf.layers.multiply()
```

**参数:**

*   **输入形状:**如果定义了该参数，它将创建另一个输入层插入到该层之前。
*   **batchInputShape:** 如果定义了这个参数，它会创建另一个输入图层，插入到这个图层之前。
*   **batchSize:** 用于构造 batchInputShape，如果尚未指定。
*   **数据类型:**指定该图层的数据类型。此参数的默认值为“float32”。
*   **名称:**指定该图层的名称。
*   **可更新:**指定是否可以通过拟合更新该图层的权重。
*   **可训练:**指定该层的权重是否可通过拟合更新。
*   **权重:**指定图层的初始权重值。
*   I**nputDType:**“float 32”或“int32”或“bool”或“complex64”或“string”。

**返回值:**与输入张量类型相同的单张量。

**例 1:**

## Javascript

```
// Import the library
import * as tf from "@tensorflow/tfjs"

const input1 = tf.input({shape: [3, 2]})
const input2 = tf.input({shape: [3, 2]})
const input3 = tf.input({shape: [3, 2]})

// Create a multiply layer
const multiplyLayer = tf.layers.multiply()

// Multiple array of inputs by applying multiplyLayer
const product = multiplyLayer.apply([input1, input2, input3])

// Print the shape of output tensor
console.log(JSON.stringify(product.shape))
```

**输出:**

```
[null,3,2]
```

**注:**此处*为空*表示批次大小未定。

**例二:**

## Javascript

```
// Import the library
import * as tf from "@tensorflow/tfjs"

// Inputs
const input1 = tf.tensor([-2, 1, 0, 5]);
const input2 = tf.tensor([3, 2, 3, 2]);
const input3 = tf.tensor([4, 3, 1, 2]);

// Create multiply layer
const multiplyLayer = tf.layers.multiply();

// Multiply inputs
const product = multiplyLayer.apply(
    [input1, input2, input3]);

// Print product
console.log(product);
```

**输出:**

```
Tensor
    [-24, 6, 0, 20]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#layers.multiply