# Tensorflow.js tf。张量类

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-tensor-class/](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-class/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

一 **tf。Tensor** 对象代表一个不可变的多维数字数组，它有一个形状和一个数据类型。张量是张量流的核心数据结构。它们是向量和矩阵向潜在更高维度的推广。

**语法:**

```
Tensor(value);
```

**属性:**该类具有以下属性:

*   **秩:**定义张量包含的维数。
*   **形状:**定义数据各个维度的大小。
*   **数据类型:**定义张量的数据类型。

**返回值:**返回一个带有提供值的 Tensor 对象。

下面的例子演示了 Tensor 类及其各种方法。

**示例 1:** 在本例中，我们将创建一个 Tensor 类，并查看 [print()方法](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-class-print-method/)的示例。此方法用于打印张量类。

## java 描述语言

```
// Importing the tensorflow library
import * as tf from "@tensorflow/tfjs"

// Creating Tensor with values
let c = tf.tensor([1, 2, 3, 4])

// Using the print() method of Tensor class
c.print();
```

**输出:**

```
Tensor
    [[1, 2],
     [3, 4]]
```

**示例 2:** 在本例中，我们将看到 Tensor 类的[克隆()方法](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-class-clone-method/)。clone()方法用于复制现有的 Tensor 类。

## java 描述语言

```
// Importing tensorflow library
import * as tf from "@tensorflow/tfjs"

// Creating Tensor class with value and [4, 1] shape
const a = tf.tensor([1, 2, 3, 4],[4,1]);

// Using the clone() method on a Tensor
let b = a.clone();

// Printing the clone Tensor
b.print();
```

**输出:**

```
Tensor[[1],
       [2],
       [3],
       [4]]
```

**示例 3:** 在本例中，我们使用了 Tensor 类的 [toString()方法](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-tostring-method/)。这种方法用于使张量类数据具有人类可读的形式。

## java 描述语言

```
// Importing tensorflow library
import * as tf from "@tensorflow/tfjs"

// Creating tensor 
const a = tf.tensor([1, 2, 3, 4]);
// Using toStirng() method in Tensor class
let b = a.toString(true);
console.log(b);
```

**示例 4:** 在本例中，我们将看到 Tensor 类的 [data()方法](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-class-data-method/)。它返回一个承诺，在解析中返回张量的值。

## java 描述语言

```
// Importing tensorflow library
import * as tf from "@tensorflow/tfjs"

// Creating tensor 
const a = tf.tensor([1, 2, 3, 4]);

// Using data method on Tensor class
let b = a.data();

b.then((x)=>console.log(x),
(b)=>console.log("Error while copying"));
```

**输出:**

```
1, 2, 3, 4
```

**示例 5:** 在本例中，我们将使用 Tensor 类的 [dataSync()方法](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-class-datasync-method/)。这个方法复制 Tensor 类的值并返回它们。

## java 描述语言

```
// Importing tensorflow library
import * as tf from "@tensorflow/tfjs"

// Creating tensor 
const a = tf.tensor([1, 2, 3, 4]);

// Using the dataSync() method
let b = a.dataSync();
console.log(b);
```

**输出:**

```
1, 2, 3, 4
```

**示例 6:** 在本例中，我们将使用 Tensor 类的 [buffer()方法](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-class-buffer-method/)。它回报了 tf 的承诺。TensorBuffer，保存底层数据的数据。

## java 描述语言

```
// Importing tensorflow library 
import * as tf from "@tensorflow/tfjs"

// Creating tensor 
const a = tf.tensor([1, 2, 3, 4]);

// Using the buffer() method on Tensor class
let b = a.buffer();

// Printing result of Promise 
 b.then((x)=>console.log(x),
 (b)=>console.log("Error while copying") );
```

**输出:**

```
TensorBuffer {
    dtype:"float32",
    shape:(1) [4],
    size:4,
    values:1,2,3,4,
    strides:(0) [ ]
}
```

**例 7:** 在本例中，我们将使用 [bufferSync()方法](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-class-buffersync-method/)。它返回一个 tf。保存底层数据的 TensorBuffer。

## java 描述语言

```
// Importing tensorflow library 
import * as tf from "@tensorflow/tfjs"
// Creating tensor 
const a = tf.tensor([1, 2, 3, 4]);
// Using bufferSync method on Tensor class
let b = a.bufferSync();

 console.log(b);
```

**输出:**

```
TensorBuffer {
dtype:"float32",
shape:(1) [4],
size:4,
values:1,2,3,4,
strides:(0) []
}
```

**示例 8:** 在本例中，我们将使用 Tensor 类的 array()方法。它以嵌套数组的形式返回张量数据的承诺。

## java 描述语言

```
// Importing tensorflow library 
import * as tf from "@tensorflow/tfjs"

// Creating tensor 
const a = tf.tensor([1, 2, 3, 4]);

// Using the array() method on Tensor class
let b = a.array();

// Printing result of Promise
b.then((x)=>console.log(x),
(b)=>console.log("Error while copying"));
```

**输出:**

```
[1, 2, 3, 4]
```

**例 9:** 在本例中，我们将使用 Tensor 类的 [arraySync()方法](https://www.geeksforgeeks.org/tensorflow-js-tf-tensor-class-arraysync-method/)。它以嵌套的形式返回张量数据。

## java 描述语言

```
// Importing tensorflow library 
import * as tf from "@tensorflow/tfjs"

// Creating tensor 
const a = tf.tensor([1, 2, 3, 4]);

// Using the arraySync() method on Tensor class
let b = a.arraySync();

console.log(b);
```

**输出:**

```
[1, 2, 3, 4]
```

**示例 10:** 在本例中，我们将使用 Tensor 类的 [dispose()方法](https://www.geeksforgeeks.org/tensorflow-js-tf-dispose-function/)。它处理 tf。记忆张量。

## java 描述语言

```
// Importing tensorflow library 
import * as tf from "@tensorflow/tfjs"

// Creating tensor 
const b = tf.tensor([1, 2, 3, 4]);

// Using the dispose() method on Tensor class
b.dispose();
b.print();
```

**输出:**

```
Tensor is disposed.
```