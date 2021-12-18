# tensorflow . js TF . initializer .截断正常()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-initializer-截短的 normal-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-initializers-truncatednormal-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**函数产生初始化为截断正态分布的随机值。**

**语法:**

```
tf.initializers.truncatedNormal(arguments)
```

**参数:**它将一个对象作为参数，该对象包含下列任何键值:

*   **均值:**是要生成的随机值的均值。
*   **stddev:** 是要生成的随机值的标准差。
*   **种子:**它**T3】是随机数发生器种子。**

**返回值:**返回

****例 1:****

## **Javascript**

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing the .initializers.truncatedNormal()
// function
let geek = tf.initializers.truncatedNormal(13)

// Printing gain value
console.log(geek);

// Printing individual gain value
console.log('\nIndividual values:\n');
console.log(geek.DEFAULT_MEAN);
console.log(geek.DEFAULT_STDDEV);
console.log(geek.mean);
console.log(geek.stddev);
```

****输出:****

```
{
  "DEFAULT_MEAN": 0,
  "DEFAULT_STDDEV": 0.05,
  "mean": 0,
  "stddev": 0.05
}

Individual values:

0
0.05
0
0.05
```

****例二:****

## **Javascript**

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs

// Defining the input value
const inputValue = tf.input({shape:[4]});

// Initializing tf.initializers.truncatedNormal()
// function
const funcValue = tf.initializers.truncatedNormal(11)

// Creating dense layer 1
const dense_layer_1 = tf.layers.dense({
    units: 4,
    activation: 'relu',
    kernelInitialize: funcValue
});

// Creating dense layer 2
const dense_layer_2 = tf.layers.dense({
    units: 6,
    activation: 'softmax'
});

// Output
const outputValue = dense_layer_2.apply(
  dense_layer_1.apply(inputValue)
);

// Creation the model.
const model = tf.model(
  {
    inputs: inputValue,
    outputs: outputValue
  });

// Predicting the output.
model.predict(tf.ones([2, 4])).print();
```

****输出:****

```
Tensor
    [[0.1830122, 0.1198884, 0.1611279, 
      0.2659391, 0.1296039, 0.1404286],
     [0.1830122, 0.1198884, 0.1611279, 
      0.2659391, 0.1296039, 0.1404286]]
```

****参考:**[https://js . tensorflow . org/API/3 . 6 . 0/#初始值设定项.截断正常](https://js.tensorflow.org/api/3.6.0/#initializers.truncatedNormal)**