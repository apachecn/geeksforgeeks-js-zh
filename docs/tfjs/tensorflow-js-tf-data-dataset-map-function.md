# tensorflow . js TF . data . dataset . map()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-dataset-map-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-dataset-map-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf.data.Dataset.map()** 函数用于通过 1 对 1 变换来映射数据集。

**语法** :

```
map(transform) 
```

**参数**:

*   **变换:**将数据集元素映射到变换后的数据集元素的函数。

**返回值**:返回 tf.data.Dataset。

**例 1:**

## Javascript

```
const gfg = tf.data.array([1, 2, 3]).map(x => x*x);

await gfg.forEachAsync(geeks => console.log(geeks));
```

**输出:**

```
1
4
9
```

**例二:**

## Javascript

```
const gfg = tf.data.array([10, 20, 30]).map(x => x+20/x);

await gfg.forEachAsync(geeks => console.log(geeks));
```

**输出:**

```
12
21
30.666666666666668
```

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.data.Dataset.map