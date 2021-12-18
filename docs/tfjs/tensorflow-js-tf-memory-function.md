# Tensorflow.js tf.memory()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-memory-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-memory-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

tensorflow . js**TF . memory()**函数用于获取程序当前时间的内存信息。此函数返回一个具有以下属性的 memoryInfo 对象:

*   **numBytes:** 指定当前分配的未公开字节数。
*   **num sensors:**它指定分配的唯一张量的数量。
*   **numDataBuffers** :指定当前时刻分配的未公开的唯一数据缓冲区个数，大于等于张量个数。
*   **不可靠:不可靠**是只有当内存使用不可靠时才为真。
*   **原因:**指定一个字符串的数组，代表内存不可靠的原因。

网络总帐属性:

*   **numBytesInGPU:** 指定当前时刻 GPU 中分配的未公开字节总数。

**语法:**

```
tf.memory() 
```

**参数:**本功能不接受任何参数。

**返回值:**返回一个 memoryInfo 对象。

**示例 1:** 打印分配张量的示例。

## java 描述语言

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs");

// Declaring a variable
let res1

// Calling tidy method
const res2 = tf.tidy(() => {

// Defining result parameter
const result = tf.scalar(121);

// Calling tf.keep() method
res1 = tf.keep(result.sqrt());

});

// Printing the number of tensors allocated at this time
console.log('numTensors: ' + tf.memory().numTensors);
```

**输出:**

```
numTensors: 1
```

**例 2:**

## java 描述语言

```
// Importing the tensorflow.js library
const tf = require("@tensorflow/tfjs");

// Declaring a variable
let res1;

// Calling tidy method
const res2 = tf.tidy(() => {
  console.log('numTensors (in tidy) : ' + tf.memory().numTensors);

  // Calling tf.keep() method with its
  // parameter
  res1 = tf.keep(tf.tensor1d(
    [1.3, 0.5, 0, NaN, null, -.5]).cos());
});

// Printing memory information
console.log('numBytes : ' + tf.memory().numBytes);
console.log('numTensors (outside tidy): ' + tf.memory().numTensors);
console.log('numDataBuffers : ' + tf.memory().numDataBuffers);
```

**输出:**

```
numTensors (in tidy) : 1
numBytes : 28
numTensors (outside tidy): 2
numDataBuffers : 2
```

**参考:**T2】https://js.tensorflow.org/api/latest/#memory