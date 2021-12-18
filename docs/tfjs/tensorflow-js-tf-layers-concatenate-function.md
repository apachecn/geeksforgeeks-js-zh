# tensorflow . js TF . layers . concatenate()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-concatenate-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-concatenate-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**tf.layers.concatenate()** 函数用于连接输入数组。

**语法:**

```
tf.layers.concatenate()
```

**参数:**

*   **参数(对象):**指定给定的对象。这是一个可选参数
*   **轴(数字):**指定输入将连接的轴。它遵循基于 0 的索引，其值必须在[-rank，rank]范围内。它可以是积极的，也可以是消极的。这里，正轴的范围从 0 到等级(值)，并指定第几个轴的尺寸。负值指定轴+等级(值)-第维度。它可以是积极的，也可以是消极的。默认值为 0。
*   **输入形状:**如果定义了该参数，它将创建另一个输入层插入到该层之前。
*   **batchInputShape:** 如果定义了这个参数，它会创建另一个输入图层，插入到这个图层之前。
*   **batchSize :** 用于构造 batchInputShape，如果尚未指定。
*   **数据类型:**指定该图层的数据类型。此参数的默认值为“float32”。
*   **名称:**指定该图层的名称。
*   **可训练:**指定该层的权重是否可通过拟合更新。
*   **权重:**指定图层的初始权重值。
*   **InputType:**“float 32”或“int32”或“bool”或“complex64”或“string”。

**返回值:**单个张量，是所有输入的串联。

**例 1:**

## java 描述语言

```
// Import the library
import * as tf from "@tensorflow/tfjs"

// Inputs
const input1 = tf.input({shape: [3, 2]})
const input2 = tf.input({shape: [3, 2]})
const input3 = tf.input({shape: [3, 2]})

// Create new concatenate layer
const concatenateLayer = tf.layers.concatenate();
const output = concatenateLayer.apply([input1, input2, input3]);

// Print shape of resulting tensor
console.log(JSON.stringify(output.shape));
```

**输出:**

```
[pre][null, 3, 6] 
```

**例 2:**

## java 描述语言

```
// Import the library
import * as tf from "@tensorflow/tfjs"

// Inputs
const input1 = tf.tensor([-2, 1, 0, 5]);
const input2 = tf.tensor([3, 2, 3, 2]);
const input3 = tf.tensor([4, 3, 1, 2]);

// Create new concatenate layer
const concatLayer = tf.layers.concatenate();
const output = concatLayer.apply([input1, input2, input3]);

// Print resulting tensor
console.log(output);
```

**输出:**

```
Tensor
    [-2, 1, 0, 5, 3, 2, 3, 2, 4, 3, 1, 2]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#layers.concatenate