# tensorflow . js TF . data . dataset 类。预取()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-dataset-class-prefetch-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-dataset-class-prefetch-method/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.data.Dataset 类。prefetch()** 函数用于产生一个数据集，该数据集从这个给定的数据集中预取指定的元素。

**语法:**

```
prefetch (bufferSize)
```

**参数:**该函数接受如下所示的参数:

*   **bufferSize:** 它是一个整数值，指定要预取的元素数量。

**返回值:**返回元素的数据集。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling the .prefetch() function over
// the specified dataset of some elements
const a = tf.data.array([5, 10, 15, 20]).prefetch(4);

// Getting the dataset of prefetched elements
await a.forEachAsync(a => console.log(a));
```

**输出:**

```
5
10
15
20
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Specifying a dataset of some elements
const a = tf.data.array(["a", "b", "c", "d", "e"]);

// Calling the .prefetch() function over
// the above dataset along with the
// batch of size 2
const b = a.batch(2)
const c = b.prefetch(2)

// Getting the dataset of prefetched elements
await c.forEachAsync(c => console.log(c));
```

**输出:**

```
Tensor
    ['a', 'b']
Tensor
    ['c', 'd']
Tensor
    ['e']
```

**参考:**T2【https://js . tensorflow . org/API/latest/# TF . data . dataset . prefetch