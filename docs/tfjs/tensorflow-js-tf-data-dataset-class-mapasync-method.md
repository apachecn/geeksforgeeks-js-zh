# tensorflow . js TF . data . dataset class . mapasync()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-dataset-class-map async-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-dataset-class-mapasync-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。mapAsync()方法**用于通过异步一对一转换来映射所述数据集。

**语法:**

```
mapAsync(transform)
```

**参数:**

*   **变换:**是将项目数据集映射到转换后的项目数据集的*承诺*的规定函数。此外，这种转换需要负责丢弃一些中间张量，如 tf.tidy()方法，其中它的计算被包装，这不能像在同步类型映射()的情况下那样在这里编程。它可以是类型(值:T) = >承诺(tf.void，number，string，TypedArray，tf。张量。Tensor[]，{[key: string]:tf。张量、数字或字符串})。

**返回值:**返回 tf.data.Dataset。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining dataset formed of an array of
// numbers and calling mapAsync() method
const res = tf.data.array([16, 12, 13]).mapAsync(
    y => new Promise(function(rsol){
        setTimeout(() => {
            rsol(y + y);
        }, Math.sqrt()*400 + 300);
}));

// Calling toArray() method and
// Printing output
console.log(await res.toArray());
```

**输出:**

```
32, 24, 26
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling mapAsync() method and
// Printing output
console.log(await tf.data.array([4.5, 8.5])
    .mapAsync(y => new Promise(function(tm) {
        setTimeout(() => {
            tm(y * y);
        })
    })).toArray());
```

**输出:**

```
20.25, 72.25
```

**参考:**[https://js . tensorflow . org/API/latest/# TF . data . dataset . mapasync](https://js.tensorflow.org/api/latest/#tf.data.Dataset.mapAsync)