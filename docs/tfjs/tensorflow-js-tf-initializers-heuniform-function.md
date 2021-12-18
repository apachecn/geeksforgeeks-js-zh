# tensorflow . js TF . initializer . heuniform()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-initializer-heuniform-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-initializers-heuniform-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**TF . initializer . heuniform()**函数从[-cap，cap]内的均匀分布中抽取样本，其中 cap 是 sqrt(6 / fan_in)。请注意， *fanIn* 是张量权重中的输入数量。

**语法:**

```
tf.initializers.heUniform(arguments)
```

**参数:**

*   **参数:**它是一个包含种子(一个数)的对象，种子是随机数生成器种子/数。

**返回值:**返回

****例 1:****

## **Javascript**

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing the .initializers.heUniform() function
const geek = tf.initializers.heUniform(7)

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
    "distribution": "uniform"
}

Individual values:

2
fanIn
uniform
```

****例二:****

## **Javascript**

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs

// Defining the input value
const inputValue = tf.input({shape:[4]});

// Initializing tf.initializers.heUniform() function
const funcValue = tf.initializers.heUniform(4)

// Creating dense layer 1
const dense_layer_1 = tf.layers.dense({
    units: 6,
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

```
Tensor
   [[0.2727611, 0.1405532, 0.0409708, 0.1262356, 
        0.1215546, 0.134949, 0.0845761, 0.0783997],
    [0.2727611, 0.1405532, 0.0409708, 0.1262356, 
        0.1215546, 0.134949, 0.0845761, 0.0783997]]
```

****参考:**[https://js . tensorflow . org/API/latest/# initializer . heuniform](https://js.tensorflow.org/api/latest/#initializers.heUniform)**