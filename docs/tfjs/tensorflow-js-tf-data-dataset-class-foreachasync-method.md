# tensorflow . js TF . data . dataset 类。forEachAsync()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-dataset-class-foreachsync-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-dataset-class-foreachasync-method/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

将函数应用于数据集的每个元素后，将使用**函数。我们可以用这个方法打印一个数组，修改数组的值等等。**

**语法:**

```
forEachAsync(f)
```

**参数:**

*   **f:** 它接受一个应用于数据集每个元素的函数

**返回值:**返回承诺

**例 1:**

## Javascript

```
// Creating an array
const arr = tf.data.array([10, 20, 30, 40, 50]);

// Applying the function on the array
await arr.forEachAsync(element => console.log(element));
```

**输出:**

```
10
20
30
40
50
```

**示例 2:** 在本例中，我们将传递一个计算元素平方的函数。

## Javascript

```
// Creating an array
const arr = tf.data.array([1, 2, 3, 4, 5]);

// Applying the function on the array
await arr.forEachAsync(element => console.log(element*element));
```

**输出:**

```
1
4
9
16
25
```

参考:[https://js . tensorflow . org/API/latest/# TF . data . dataset . foreachasync](https://js.tensorflow.org/api/latest/#tf.data.Dataset.forEachAsync)