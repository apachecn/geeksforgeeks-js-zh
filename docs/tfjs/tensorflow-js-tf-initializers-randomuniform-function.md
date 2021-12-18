# tensorflow . js TF . initializer . randomuniform()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-initializer-random uniform-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-initializers-randomuniform-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**TF . initializer . randomuniform()**函数生成初始化为均匀分布的随机值。这些值在配置的最小值和最大值之间均匀分布。

**语法:**

```
tf.initializers.randomUniform(arguments)
```

**参数:**

*   **参数:**它是一个包含下面列出的 3 个键值的对象:
    1.  **均值:**是要生成的随机值的均值。
    2.  **stddev:** 是要生成的随机值的标准差。
    3.  **种子:**它**T3】是随机数发生器种子。**

**返回值:**返回

****例 1:****

## **Javascript**

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing the .initializers.randomUniform() function
let geek = tf.initializers.randomUniform(5)

// Printing gain value
console.log(geek);

// Printing individual gain value.
console.log('\nIndividual values:\n');
console.log(geek.DEFAULT_MINVAL);
console.log(geek.DEFAULT_MAXVAL);
console.log(geek.minval);
console.log(geek.maxval);
```

****输出:****

```
{
  "DEFAULT_MINVAL": -0.05,
  "DEFAULT_MAXVAL": 0.05,
  "minval": -0.05,
  "maxval": 0.05
}

Individual values:

-0.05
0.05
-0.05
0.05
```

****例二:****

## **Javascript**

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs

// Defining the input value
const inputValue = tf.input({shape:[4]});

// Initializing tf.initializers.randomUniform() function.
const funcValue = tf.initializers.randomUniform(8)

// Creating dense layer 1
const dense_layer_1 = tf.layers.dense({
    units: 5,
    activation: 'relu',
    kernelInitialize: funcValue
});

// Creating dense layer 2
const dense_layer_2 = tf.layers.dense({
    units: 7,
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
    [[0.1145501, 0.133405, 0.0640167, 0.2349582, 
     0.1064994, 0.0799759, 0.2665946],
     [0.1145501, 0.133405, 0.0640167, 0.2349582, 
      0.1064994, 0.0799759, 0.2665946]]
```

****参考:**[**https://js . tensorflow . org/API/3 . 6 . 0/# initializer . randomuniform**](https://js.tensorflow.org/api/3.6.0/#initializers.randomUniform)**