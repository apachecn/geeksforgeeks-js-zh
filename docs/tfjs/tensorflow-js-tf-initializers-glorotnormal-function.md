# tensorflow . js TF . initializer . glrotnormal()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-initializer-glrotnormal-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-initializers-glorotnormal-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**TF . initializer . glrotnormal()**函数从以 0 为中心的截断正态分布中提取样本，其中*stddev = sqrt(2/(fan _ in+fan _ out))*。请注意，*扇入*是张量权重中的输入数量，*扇出*是张量权重中的输出数量。

**语法:**

```
tf.initializers.glorotNormal(arguments)
```

**参数:**

*   **参数:**它是一个包含种子(一个数)的对象，种子是随机数生成器种子/数。

**返回值:**返回

****例 1:****

## **Javascript**

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing the .initializers.glorotNormal() function
console.log(tf.initializers.glorotNormal(9));

// Printing Individual gainvalues
console.log('\nIndividual values:\n');
console.log(tf.initializers.glorotNormal(9).scale);
console.log(tf.initializers.glorotNormal(9).mode);
console.log(tf.initializers.glorotNormal(9).distribution);
```

****输出:****

```
{
    "scale": 1,
    "mode": "fanAvg",
    "distribution": "normal"
}

Individual values:

1
fanAvg
normal
```

****例二:****

## **Javascript**

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs

// Defining the input value
const inputValue = tf.input({ shape: [4] });

// Initializing tf.initializers.glorotNormal() function
const funcValue = tf.initializers.glorotNormal(9)

// Creating dense layer 1
const dense_layer_1 = tf.layers.dense({
    units: 11,
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
    [[0.1004296, 0.1564845, 0.1716817, 0.1526613, 
            0.1739253, 0.1059624, 0.1388552],
     [0.1004296, 0.1564845, 0.1716817, 0.1526613, 
            0.1739253, 0.1059624, 0.1388552]]
```

****参考:**[https://js . tensorflow . org/API/latest/# initializer . glrotnormal](https://js.tensorflow.org/api/latest/#initializers.glorotNormal)**