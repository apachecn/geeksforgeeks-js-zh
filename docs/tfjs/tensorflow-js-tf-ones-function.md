# tensorflow . js TF . one()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-one-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-ones-function/)

Tensorflow.js 是一个开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。**TF . one()**函数用于创建一个新的张量，其中所有元素都设置为 1。

**语法:**

```
tf.ones(shape, dtype, name)
```

**参数:**

*   **Shape:** It takes the shape of a tensor. It can be a multidimensional array or int32.
*   **Data type:** Take the data type of 1 we are inserting. The default setting is float32, but it can also be int32\. This is an optional parameter.
*   **Name:** Take the name of the operation we are executing. By default, it is None. This is an optional parameter.

**返回值:**返回数据类型相同的张量。

**示例 1:** 在本例中，我们将创建一个 2D 张量，其所有值都设置为整数数据类型的 1。

## JavaScript

```
// Import tensorflow
import tensorflow as tf

// Get a Tensor
val = tf.ones([10, 10], tf.int32)

// Print the Tensor
print(val)
```

**输出:**

```
tf.Tensor(
[[1 1 1 1 1 1 1 1 1 1]
 [1 1 1 1 1 1 1 1 1 1]
 [1 1 1 1 1 1 1 1 1 1]
 [1 1 1 1 1 1 1 1 1 1]
 [1 1 1 1 1 1 1 1 1 1]
 [1 1 1 1 1 1 1 1 1 1]
 [1 1 1 1 1 1 1 1 1 1]
 [1 1 1 1 1 1 1 1 1 1]
 [1 1 1 1 1 1 1 1 1 1]
 [1 1 1 1 1 1 1 1 1 1]], shape=(10, 10), dtype=int32)
```

**示例 2:** 在本例中，我们将创建一个 1D 张量，其所有值都设置为浮点数据类型的 1。

## JavaScript

```
// Import tensorflow
import tensorflow as tf

// Get a Tensor
val = tf.ones(5, tf.float32)

// Print a Tensor
print(val)
```

**输出:**

```
tf.Tensor([1\. 1\. 1\. 1\. 1.], shape=(5,), dtype=float32)
```

**参考:**T2】https://js.tensorflow.org/api/latest/#ones