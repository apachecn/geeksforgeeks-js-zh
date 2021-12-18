# Tensorflow.js tf。TensorBuffer 类。get()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-tensorbuffer-class-get-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-tensorbuffer-class-get-method/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf。TensorBuffer 类。get()** 方法用于返回给定位置的指定缓冲区中的值。

**语法:**

```
get (...locations)
```

**参数:**该方法接受单个参数，如下图所示:

*   **位置:**指定的位置索引。

**返回值:**返回指定位置索引处的值。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a buffer of 2*2 dimensions
const buffer = tf.buffer([2, 2]); 

// Setting values at particular indices. 
buffer.set(5, 0, 0); 
buffer.set(10, 1, 0); 

// Getting the values for the
// specified indices with the
// help of .get() function
console.log(buffer.get(0, 0));
console.log(buffer.get(1, 0));
```

**输出:**

```
5
10 
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a buffer of 3*3 dimensions
const buffer = tf.buffer([3, 3]); 

// Setting values at particular indices. 
buffer.set(5, 0, 0); 
buffer.set(10, 0, 1); 
buffer.set(15, 1, 0); 
buffer.set(20, 1, 1); 
buffer.set(25, 2, 0); 
buffer.set(30, 2, 1); 
buffer.set(35, 2, 2); 

// Getting the values for the
// specified indices with
// the help of .get() functions
console.log(buffer.get(0, 0));
console.log(buffer.get(0, 1));
console.log(buffer.get(1, 0));
console.log(buffer.get(2, 0));
console.log(buffer.get(2, 1));
console.log(buffer.get(2, 2));
```

**输出:**

```
5
10
15
25
30
35
```

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.TensorBuffer.get