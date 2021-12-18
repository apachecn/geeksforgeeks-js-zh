# tensorflow . js TF . data . dataset . foreachasync()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-dataset-foreachasync-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-dataset-foreachasync-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

将函数应用于数据集的每个元素后，将使用**函数**

**语法** :

```
forEachAsync(f)
```

**参数**:

*   **f:** 应用于每个数据集元素的函数。

**返回值**:返回承诺<作废>

**例 1:**

## Javascript

```
const a = tf.data.array([1, 2, 3]);
await a.forEachAsync(e => console.log(e));
```

**输出:**

```
1
2
3
```

**例二:**

## Javascript

```
const a = tf.data.array([1, 2, 3]);
await a.forEachAsync(e => console.log(e*2));
```

**输出:**

```
2
4
6
```

**参考:**[https://js . tensorflow . org/API/latest/# TF . data . dataset . foreachasync](https://js.tensorflow.org/api/latest/#tf.data.Dataset.forEachAsync)