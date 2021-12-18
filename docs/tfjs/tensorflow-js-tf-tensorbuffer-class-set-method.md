# Tensorflow.js tf。TensorBuffer 类。设置()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-tensorbuffer-class-set-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-tensorbuffer-class-set-method/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf。TensorBuffer 类。set()** 功能用于在缓冲区的指定位置设置给定值。

**语法:**

```
set (value, ...locations)
```

**参数:**该函数接受两个参数，如下图所示:

*   **值:**要设置的指定值。
*   **位置:**指定的位置索引。

**返回值:**不返回值。

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

// Converting the above buffer
// back to a tensor value to print
buffer.toTensor().print();
```

**输出:**

```
Tensor
   [[5 , 0],
    [10, 0]]
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

// Converting the above buffer
// back to a tensor value to print
buffer.toTensor().print()
```

**输出:**

```
Tensor
   [[5 , 10, 0 ],
    [15, 20, 0 ],
    [25, 30, 35]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.TensorBuffer.set