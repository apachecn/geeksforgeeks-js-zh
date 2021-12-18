# Tensorflow.js tf.data.array()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-array-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-array-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**.data.array()方法**用于基于由元素组成的数组形成数据集。

**语法:**

```
tf.data.array(items)
```

**参数:**

*   **项:**它是由要在像项这样的数据集中解析的元素组成的声明数组，可以是 tf.void、number、string、TypedArray、tf 类型。张量。Tensor[]，或{[key: string]:tf。张量、数字或字符串}[]。

**返回值:**返回 tf.data.Dataset。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining dataset formed of an array
// of objects and calling data.array()
const res = tf.data.array([
    {'element': 5}, 
    {'element': 6}, 
    {'element': 7}
]);

// Calling forEachAsync() method and
// Printing output
await res.forEachAsync(op => console.log(op));
```

**输出:**

```
{
  "element": 5
}
{
  "element": 6
}
{
  "element": 7
}
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining dataset formed of an array
// of numbers and calling data.array()
const res = tf.data.array([4.6, 7.9, 9.6, 2.6, 8.9]);

// Calling forEachAsync() method and
// Printing output
await res.forEachAsync(op => console.log(op));
```

**输出:**

```
4.6
7.9
9.6
2.6
8.9
```

**参考:**T2】https://js.tensorflow.org/api/latest/#data.array