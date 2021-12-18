# tensorflow . js TF . data . dataset 类

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-dataset-class/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-dataset-class/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

tensorflow . js**TF . data . dataset 类**代表大量的数据集合。数据可以是数组、映射或基元，也可以是这种数据类型的任何嵌套结构。数据类型在一些有序的数据集合中。我们可以对这些数据执行各种方法。此方法会生成一个新的数据集。

**语法:**

```
tf.data.method(args);
```

**参数:**该方法接受以下参数:

*   **args:** 不是所有方法都一样，不同方法可以不同。

**返回值:**返回与输入相同类型的数据集。

**示例 1:** 在本例中，我们将看到 batch()方法。它将元素分批分组。它接受两个参数 batchSize，batchSize 是组的长度，smallLastBatch 是一个布尔值，告诉打印最后一批，如果它的长度很小。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs")

// Creating tenst dataset of array
const array = [[1, 4, 6], [2, 5, 7],
    [3, 6, 8], [4, 7, 9], [5, 8, 11]];

// Making dataset with array
const gfg = tf.data.array(array);

// Creating new dataset
const GFG = gfg.batch(2);

// Printing Dataset
GFG.forEachAsync(Q => Q.print());
```

**输出:**

```
Tensor
    [[1, 4, 6],
     [2, 5, 7]]
Tensor
    [[3, 6, 8],
     [4, 7, 9]]
Tensor
     [[5, 8, 11],]
```

**示例 2:** 在本例中，我们将看到 shuffle()方法。它用于洗牌数据集中的元素。它采用缓冲区大小，缓冲区大小是 shuffle 元素将从其开始的数字，seed 用于为元素的分布创建随机种子，或者最后一个参数是 resump each _ iteration，这是一个布尔值，它告诉在迭代数据集时随机重新洗牌。

## Javascript

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs")

// Creating Dataset  
const gfg_array = [4, 8, 12, 16, 20];
const gfg = tf.data.array(gfg_array);

// Prefetching data from dataset
const GFG_array = gfg.shuffle(5);

// Printing data from array
GFG_array.forEachAsync( tm => console.log(tm))
```

**输出:**

```
8
20
4
16
12
```

**参考:**T2】https://js.tensorflow.org/api/latest/#class:data.Dataset