# tensorflow . js TF . data . dataset . repeat()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-dataset-repeat-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-dataset-repeat-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf.data.Dataset.repeat()** 函数用于重复数据集计数时间

**语法** :

```
repeat (count?)
```

**参数**

*   **计数:**一个整数，表示数据集应该重复的次数。

**返回值**:返回 tf.data.Dataset。

**例 1:**

## Javascript

```
const a = tf.data.array([1, 2, 3]).repeat(3);

await a.forEachAsync(e => console.log(e)),
```

**输出:**

```
​1
2
3
1
2
3
1
2
3
```

**例二:**

## Javascript

```
const a = tf.data.array([2, 4, 6]).repeat(5);

await a.forEachAsync(e => console.log(e*2));
```

**输出:**

```
4
8
12
4
8
12
4
8
12
4
8
12
4
8
12
```

**参考:**[https://js . tensorflow . org/API/latest/# TF . data . dataset . repeat](https://js.tensorflow.org/api/latest/#tf.data.Dataset.repeat)