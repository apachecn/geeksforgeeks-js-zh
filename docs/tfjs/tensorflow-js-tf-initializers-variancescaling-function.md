# tensorflow . js TF . initializer . variancescaling()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-initializer-variance scaling-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-initializers-variancescaling-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**TF . initializer . variance scaling()**函数能够根据权重的形状调整其比例。使用分布=NORMAL 的值，从中心为 0 的截断正态分布中抽取样本，其中 *stddev = sqrt(scale / n)。*注意，n 的值变化如下:

*   If mode = FAN_IN, it is the number of inputs in tensor weight.
*   If mode = the value of fan _ out, it is the number of outputs in tensor weight.
*   If the value of mode = FAN_AVG, it is the average of output and input in tensor weight.

**语法:**

```
tf.initializers.varianceScaling(arguments)
```

**参数:**它将一个对象作为参数，该对象包含下面列出的 3 个键值:

*   **刻度:**是刻度因子。它是一个正浮点值。
*   **模式:**是输出和输入的扇动模式。
*   **分布:**是数值的概率分布。
*   **种子:**它**T3】是随机数发生器种子。**

**返回值:**返回

****例 1:****

## **Javascript**

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing the .initializers.varianceScaling()
// function
let geek = tf.initializers.varianceScaling(33)

// Printing gain value
console.log(geek);

// Printing individual gain value.
console.log('\nIndividual values:\n');
console.log(geek.scale);
console.log(geek.mode);
console.log(geek.distribution);
```

****输出:****

```
{
  "scale": 1,
  "mode": "fanIn",
  "distribution": "normal"
}

Individual values:

1
fanIn
normal
```

****例二:****

## **Javascript**

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs

// Defining the input value
const inputValue = tf.input({shape:[4]});

// Initializing tf.initializers.varianceScaling() function
const funcValue = tf.initializers.varianceScaling(3)

// Creating dense layer 1
const dense_layer_1 = tf.layers.dense({
    units: 5,
    activation: 'relu',
    kernelInitialize: funcValue
});

// Creating dense layer 2
const dense_layer_2 = tf.layers.dense({
    units: 9,
    activation: 'softmax'
});

// Output
const outputValue = dense_layer_2.apply(
    dense_layer_1.apply(inputValue)
);

// Creation the model.
const model = tf.model({
    inputs: inputValue,
    outputs: outputValue
});

// Predicting the output.
model.predict(tf.ones([2, 4])).print();
```

****输出:****

```
Tensor
    [[0.0687333, 0.1549079, 0.0899771, 0.084183, 
      0.1593787, 0.1488634, 0.0884578, 0.073244, 0.1322549],
     [0.0687333, 0.1549079, 0.0899771, 0.084183, 
      0.1593787, 0.1488634, 0.0884578, 0.073244, 0.1322549]]
```

****参考:**[https://js . tensorflow . org/API/3 . 6 . 0/# initializer . variance scaling](https://js.tensorflow.org/api/3.6.0/#initializers.varianceScaling)**