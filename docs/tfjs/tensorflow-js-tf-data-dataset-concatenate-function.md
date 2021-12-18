# tensorflow . js TF . data . dataset . concatenate()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-dataset-concatenate-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-dataset-concatenate-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**函数用于将数据集与另一个数据集连接起来。**

**语法** :

```
concatenate(dataset)
```

**参数:**

*   **数据集:**要连接到此数据集的数据集。

**返回值**:返回 tf.data.Dataset

**例 1:**

## Javascript

```
const gfg = tf.data.array([1, 2, 3]);
const geeks = tf.data.array([6, 5, 4]);
const gfg1 = geeks.concatenate(gfg);
await gfg1.forEachAsync(e => console.log(e));
```

**输出:**

```
6
5
4
1
2
3
```

**例二:**

## Javascript

```
const gfg = tf.data.array(['a', 'b', 'c', 'd']);
const geeks = tf.data.array([6, 5, 4]);
const gfg1 = geeks.concatenate(gfg);
console.log(gfg1);
```

**输出:**

```
{
  "size": 7
}
```

**参考:**T2【https://js . tensorflow . org/API/latest/# TF . data . dataset . concatenate