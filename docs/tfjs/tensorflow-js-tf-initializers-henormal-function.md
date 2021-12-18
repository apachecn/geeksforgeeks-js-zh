# tensorflow . js TF . initializer . Henormal()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-initializer-he normal-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-initializers-henormal-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**函数从以零为中心的截断正态分布中抽取样本，其中 *stddev = sqrt(2 / fanIn)* 在[-limit，limit]范围内，其中 limit 为 *sqrt(6 / fan_in)* 。请注意，fanIn 是张量权重中的输入数量。**

**语法:**

```
tf.initializers.heNormal(arguments)
```

**参数:**

*   **参数:**它是一个包含种子(一个数)的对象，种子是随机数生成器种子/数。

**返回值:**返回

****例 1:****

## **java 描述语言**

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing the .initializers.heNormal()
// function
const geek = tf.initializers.heNormal(7)

// Printing gain
console.log(geek);
console.log('\nIndividual values:\n');
console.log(geek.scale);
console.log(geek.mode);
console.log(geek.distribution);
```

****输出:****

```
{
  "scale": 2,
  "mode": "fanIn",
  "distribution": "normal"
}

Individual values:

2
fanIn
normal
```

****例 2:****

## **java 描述语言**

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs

// Defining the input value
const inputValue = tf.input({shape:[4]});

// Initializing tf.initializers.heNormal() function
const funcValue = tf.initializers.heNormal(3)

// Creating dense layer 1
const dense_layer_1 = tf.layers.dense({
    units: 7,
    activation: 'relu',
    kernelInitialize: funcValue
});

// Creating dense layer 2
const dense_layer_2 = tf.layers.dense({
    units: 8,
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

> **张量
> 【【0.0802892，0.1482767，0.1004469，0.1141223，0.218376，0.1217001，0.139549，0.0772399】，
> 【0.0802892，0.1482767，0.1004469，0.1114044469**

****参考:**T2】https://js.tensorflow.org/api/latest/#initializers.heNormal**