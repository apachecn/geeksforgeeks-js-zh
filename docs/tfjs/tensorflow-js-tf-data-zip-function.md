# Tensorflow.js tf.data.zip()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-zip-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-zip-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf.data.zip()** 函数用于通过将数据集的字典、数组或嵌套结构压缩在一起来创建数据集。

**语法:**

```
tf.data.zip(datasets)
```

**参数:**

*   **数据集:**是数据集。

**返回值:**返回 tf.data.Dataset。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing Array dataset.
let geek1 = tf.data.array([1, 2, 3, 4]);
let geek2 = tf.data.array([5, 6, 7, 8]);

// Ziping dataset of objects.
let geek3 = tf.data.zip([geek1, geek2]);

// Printing the returned promise.  
await geek3.forEachAsync(function(geek){
  console.log(JSON.stringify(geek))
});
```

**输出:**

```
[1,5]
[2,6]
[3,7]
[4,8]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Ziping two array dataset.
let geek = tf.data.zip({
    geek1: tf.data.array([1, 2, 3, 4]), 
    geek2: tf.data.array([5, 6, 7, 8])
});

// Printing the result.
await geek.forEachAsync(function(e){
  console.log(JSON.stringify(e))
});
```

**输出:**

```
{"geek1":1,"geek2":5}
{"geek1":2,"geek2":6}
{"geek1":3,"geek2":7}
{"geek1":4,"geek2":8}
```

**参考资料:**[https://js . tensorlow . org/API/3 . 6 . 0/# TF . data . zip](https://js.tensorflow.org/api/3.6.0/#tf.data.zip)