# Tensorflow.js tf.layers.dot()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-dot-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-dot-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。Tensorflow.js tf.layers.dot()函数用于应用所提供的两个张量之间的点积。

**语法:**

```
tf.layers.dot(args);
```

**参数:**该函数接受以下参数:

*   **Parameter:** It is an object with the following fields:
    *   **Axis:** It defines the axis in which direction to dot the product.
    *   **normalize:** is Boolean data used to generate the answer of dot product in cosine value form.
    *   **Input shape:** Defines the shape of the model input layer. It is used to create the input layer.
    *   **Data type:** is the data type of the layer. It is used for the first layer of the model.
    *   **Name:** The string is the name of the input layer.
    *   **Weight:** It is a tensor whose value is the initial value of the layer.
    *   **Trainable:** Defines whether the layer can be trained or not. It is a Boolean data type.
    *   [T0】 batchInputShape: 【T1] Define the shape of the batch for the samples in the input layer. It is used to make the input layer.
    *   **batchsize:** It is used as a supplement to batchInputShape in the construction of input layer. It is used to make the input layer.
    *   [T0】 input type: 【T1] is the data type of the input data in the layer.

**返回:**返回两个张量的乘积张量。

下面是这个函数的一些例子。

**示例 1:** 在本例中，我们将简单地制作一个张量与-2 轴旋转值的点积。

## Javascript

```
// import * as tf from "@tensorflow/tfjs"

// Generating tensor of [3,3] shape and size.
const geek_tens1 = tf.randomUniform([3 ,3]);
const geek_tens2 = tf.randomUniform([3 ,3]);

// Making tensor campatiable to apply to dot product.
const geek_Input = [geek_tens1 ,geek_tens2];

// Calling dot product
const geek_config = {axes: -2};
const geek_DotPro = tf.layers.dot(geek_config);
const geek_DotProRes = geek_DotPro.apply(geek_Input);

// Printing our result
console.log(geek_DotProRes);
geek_DotProRes.print();
```

**输出:**

```
Tensor
    [[0.7034817],
     [0.2338114],
     [1.1493738]]
Tensor
    [[0.7034817],
     [0.2338114],
     [1.1493738]]
```

**例 2:** 在这个例子中，我们将做两个张量的点积，看到余弦形式的结果。

## Javascript

```
import * as tf from "@tensorflow/tfjs"

// Collect both outputs and print separately.
// Generating tensor of [3,3] shape and size.
const geek_tens1 = tf.randomUniform([2 ,4]);
const geek_tens2 = tf.randomUniform([2 ,4]);

// Making tensor campatiable to apply to dot product.
const geek_Input = [geek_tens1 ,geek_tens2];

// Calling dot product
const geek_config = {axis: 1, normalize: true,
        dtype: 'int32', name: 'DotProduct' };
const geek_DotPro = tf.layers.dot(geek_config);
const geek_DotProRes = geek_DotPro.apply(geek_Input);

// Printing our result
console.log(geek_DotProRes);
```

**输出:**

```
Tensor
    0.6817111968994141
```

**参考:**T2】https://js.tensorflow.org/api/latest/#layers.dot