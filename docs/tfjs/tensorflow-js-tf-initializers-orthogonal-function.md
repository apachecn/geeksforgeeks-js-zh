# tensorflow . js TF . initializer .正交()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-initializer-正交-函数/](https://www.geeksforgeeks.org/tensorflow-js-tf-initializers-orthogonal-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

函数的作用是:产生一个随机的正交矩阵。

**语法:**

```
tf.initializers.orthogonal(arguments)
```

**参数:**

*   **参数:**它是一个包含种子(一个数)和增益(一个数)的对象，种子(一个数)是随机数生成器种子，增益(一个数)是要应用于正交矩阵的乘法因子。它的默认值被认为是 1。

**返回值:**返回

****例 1:****

## **Javascript**

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing the .initializers.orthogonal() function
let geek = tf.initializers.orthogonal(2)

// Printing gain value
console.log(geek);

// Printing individual gain value
console.log('\nIndividual values:\n');
console.log(geek.DEFAULT_GAIN);
console.log(geek.gain);
```

****输出:****

```
{
  "DEFAULT_GAIN": 1,
  "gain": 1
}

Individual values:

1
1
```

****例二:****

## **Javascript**

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs

// Defining the input value
const inputValue = tf.input({shape:[4]});

// Initializing tf.initializers.orthogonal() function
const funcValue = tf.initializers.orthogonal(4)

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
    [[0.0925488, 0.0833014, 0.1223793, 0.1189993, 
      0.0733501, 0.1645982, 0.1299256, 0.2148973],
     [0.0925488, 0.0833014, 0.1223793, 0.1189993, 
      0.0733501, 0.1645982, 0.1299256, 0.2148973]]
```

****参考:**[**https://js . tensorflow . org/API/3 . 6 . 0/# initializer .正交**](https://js.tensorflow.org/api/3.6.0/#initializers.orthogonal)**