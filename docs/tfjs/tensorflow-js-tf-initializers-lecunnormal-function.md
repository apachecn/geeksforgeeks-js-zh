# tensorlow . js TF . initiators . lecunnnormal()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-initializer-lecunnormal-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-initializers-lecunnormal-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**TF . initializer . lecunnormal()**函数从截断正态分布中提取样本，该分布以零为中心，stddev = sqrt(1 / fanIn)。注意 *fanIn* 是张量权重中的输入数。

**语法:**

```
tf.initializers.leCunNormal(arguments).
```

**参数:**

*   **参数:**它是一个包含种子(一个数)的对象，种子是随机数生成器种子/数。

**返回值:**返回

****例 1:****

## **java 描述语言**

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Initializing the .initializers.leCunNormal() function
const geek = tf.initializers.leCunNormal(3)

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
    "scale": 1,
    "mode": "fanIn",
    "distribution": "normal"
}

Individual values:

1
fanIn
normal
```

****例 2:****

## **java 描述语言**

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Defining the input value
let inputValue = tf.input({ shape: [4] });

// Initializing tf.initializers.leCunNormal()
// function
let funcValue = tf.initializers.leCunNormal(7)

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
    [[0.0666204, 0.1171203, 0.2322821, 0.1056982, 
            0.2149536, 0.1846998, 0.0786256],
     [0.0666204, 0.1171203, 0.2322821, 0.1056982, 
            0.2149536, 0.1846998, 0.0786256]]
```

****参考:**T2【https://js . tensorflow . org/API/latest/# initializer . lecunnormal**