# tensorflow . js TF . layers . flat()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-flat-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-flatten-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**TF . layers . flat()**功能用于展平输入，不影响批次大小。展平层将输入中的每个批次展平为一维。

**语法:**

```
tf.layers.flatten( args? )
```

**参数:**它将一个对象作为输入:args (Object)。提供 args 对象作为输入是可选的。以下是您可以在 args 对象中提供的字段。

*   **数据格式(‘通道优先’或‘通道最后’):**是图像数据格式。
*   **input shape((null | number)[]):**用于创建一个输入图层插入到该图层之前。
*   **batchInputShape((null | number)[]):**用于创建一个输入图层插入到该图层之前。如果同时定义了输入形状和批处理输入形状，将使用批处理输入形状。
*   **batchSize(数字):**如果指定了 inputShape 而没有指定 batchInputShape，则 batchSize 用于构造 batchInputShape。
*   **数据类型(' float 32 ' | ' int 32 ' | ' bool ' | ' complex 64 ' | ' string '):**用于定义该层的数据类型。
*   **名称(字符串):**用于为图层提供名称。
*   **可训练(布尔):**用于指定该层的权重是否可通过拟合更新。默认值为真。
*   **重量(tf。Tensor[]):** 用于提供图层的初始权重值。

**返回值:**返回展平的图层。

**例 1:**

## Javascript

```
const tf = require("@tensorflow/tfjs")

const input = tf.input({shape: [5, 4]});

// Creating flattened layer
const flattenLayer = tf.layers.flatten();

// Printing the shape
console.log(JSON.stringify(flattenLayer.apply(input).shape));
```

**输出:**在输出中，我们可以看到展平图层的形状等于`[null，12]`，因为第二维是 4 * 3，即展平的结果。

```
[null, 20]
```

**示例 2:** 在本例中，我们将提供 args 对象中的名称字段作为输入。

## Javascript

```
const tf = require("@tensorflow/tfjs")

const input = tf.input({shape: [4, 3]});

// Creating flattened layer
const flattenLayer = tf.layers.flatten({name:'NewLayer1'});

// Printing the name and shape
console.log("Name of the layer: " 
    + flattenLayer.apply(input).name)

console.log(JSON.stringify(
    flattenLayer.apply(input).shape));
```

**输出:**

```
Name of the layer: NewLayer1/NewLayer1
[null, 12]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#layers.flatten