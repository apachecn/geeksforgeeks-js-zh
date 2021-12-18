# tensorflow . js TF . initializer . glrotuniform()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-initializer-glrotuniform-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-initializers-glorotuniform-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**TF . initializer . glrotuniform()**函数从【-limit，limit】内的均匀分布中提取样本，其中 limit 为 *sqrt(6 / (fan_in + fan_out))* 其中 fan_in 为权重张量中的输入单位数，fan_out 为权重张量中的输出单位数

**语法:**

```
tf.initializers.glorotUniform(arguments).
```

**参数:**

*   **参数:**它是一个包含种子(一个数)的对象，种子是随机数生成器种子/数。

**返回值:**返回

****例 1:****

## **Javascript**

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Initializing the .initializers.glorotUniform() function
const geek = tf.initializers.glorotUniform(7)

// Printing gain value
console.log(geek);

// Printing individual values from gain
console.log('\nIndividual values:\n');
console.log(geek.scale);
console.log(geek.mode);
console.log(geek.distribution);
```

****输出:****

```
{
  "scale": 1,
  "mode": "fanAvg",
  "distribution": "uniform"
}

Individual values:

1
fanAvg
uniform
```

****例二:****

## **Javascript**

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Defining the input value
let inputValue = tf.input({shape:[4]});

// Initializing tf.initializers.glorotUniform() function
let funcValue = tf.initializers.glorotUniform(7)

// Creating dense layer 1
let dense_layer_1 = tf.layers.dense({
    units: 5,
    activation: 'relu',
    kernelInitialize: funcValue
});

// Creating dense layer 2
let dense_layer_2 = tf.layers.dense({
    units: 7,
    activation: 'softmax'
});

// Output
let outputValue = dense_layer_2.apply(
    dense_layer_1.apply(inputValue)
);

// Creation the model.
let model = tf.model({
    inputs: inputValue,
    outputs: outputValue
});

// Predicting the output
let finalOutput = model.predict(tf.ones([2, 4]));
finalOutput.print();
```

****输出:****

```
Tensor
    [[0.0809571, 0.1913243, 0.1932435, 0.1622382,
            0.2768594, 0.046838, 0.0485396],
     [0.0809571, 0.1913243, 0.1932435, 0.1622382, 
            0.2768594, 0.046838, 0.0485396]]
```

****参考:**[https://js . tensorflow . org/API/latest/# initializer . glrotuniform](https://js.tensorflow.org/api/latest/#initializers.glorotUniform)**