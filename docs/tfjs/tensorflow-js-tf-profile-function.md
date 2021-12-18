# Tensorflow.js tf.profile()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-profile-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-profile-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf.profile()** 函数用于执行所提供的函数，并且该函数返回一个 Promise，该 Promise 使用关于其内存使用的信息进行解析。

**语法:**

```
tf.profile(f);
```

**参数:**

*   **f:** 是回调函数。

**返回值:**返回承诺。

**例:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing tensor and 
// Using .profile() function 
let geekProfile =
   await tf.profile(function (){
   let geek1 = tf.tensor2d([[1, 2, 3], [4, 5, 6]]);
   geek1.square();
   return geek1;
});

// Printing the result of returned Promise
console.log("peakBytes: ")
console.log(geekProfile.peakBytes);
console.log("kernelName: ");
console.log(geekProfile.kernelNames);
```

**输出:**

```
peakBytes: 
48
kernelName: 
Square
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing tensor and 
// Using .profile() function 
let geekProfile =
   await tf.profile(function (){
   let geek2 = tf.tensor4d([[[[7], [11]], [[13], [34]]]]);
   return geek2;
});

// Printing the result of returned Promise
console.log("newBytes ")
console.log(geekProfile.newBytes);
```

**输出:**

```
newBytes 
16
```

**参考:**T2】https://js.tensorflow.org/api/latest/#profile