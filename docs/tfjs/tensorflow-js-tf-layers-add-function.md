# Tensorflow.js tf.layers.add()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-add-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-add-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

当提供多个数组作为输入时， **tf.layers.add()** 函数用于计算每个元素的加法。

**语法** :

```
tf.layers.add().apply([input1, input2,input3,......,inputn])
```

**参数:**

*   **输入形状:**这是一个可选参数，用于创建输入图层，它采用数字和空值等值。
*   **batchInputShape:** 是一个可选参数，用于在主图层之前创建输入图层，取数值如 number 和 null。
*   **batchSize:** 它是用于制作 batchInputShape 的可选参数，只接受数字。
*   **数据类型:**可选参数，代表数据类型。默认情况下，它有“float32”，还支持其他值，如“int32”、“bool”等。
*   **名称:**为可选参数，用于定义图层名称，接受字符串。
*   **可训练**:是一个可选参数，决定提供的输入图层是否更新。它接受布尔值。
*   **权重:**拥有图层的起始权重。它也是一个可选参数。
*   **输入类型:**是用于输入数据类型的可选参数。像 dtype 一样，它也支持它的所有值。

**返回值:**返回 Add。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

const input1 = tf.input({shape: [90.5, 3]});
const input2 = tf.input({shape: [90.5, 3]});
const addLayer = tf.layers.add();
const sum = addLayer.apply([input1, input2]);
console.log(JSON.stringify(sum.shape));
```

**输出:**

```
[null,90.5,3]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

const input1 = tf.input({shape: [127.65, 56]});
const input2 = tf.input({shape: [127.65, 56]});
const input3 = tf.input({shape: [127.65, 56]});
const input4 = tf.input({shape: [127.65, 56]});
const input5 = tf.input({shape: [127.65, 56]});
const input6 = tf.input({shape: [127.65, 56]});
const input7 = tf.input({shape: [127.65, 56]});
const input8 = tf.input({shape: [127.65, 56]});

const addLayer = tf.layers.add();
const sum = addLayer.apply([input1, input2, input3, 
          input4, input5, input6, input7, input8]);

console.log(JSON.stringify(sum.shape));
```

**输出:**

```
[null,127.65,56]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#layers.add