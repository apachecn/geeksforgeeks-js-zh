# tensorflow . js TF . constraints . constraints 类

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-constraints-constraints-class/](https://www.geeksforgeeks.org/tensorflow-js-tf-constraints-constraint-class/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。 **tf.constraints.Constraint 类**用于扩展**序列化。可序列化类**。此外，它是支持对权重值实施约束的函数的基类。

这个 tf.constraints.Constraint 类包含四个内置函数，如下所示:

*   TF。约束。限制类 [.constraints.maxNorm()](https://www.geeksforgeeks.org/tensorflow-js-tf-constraints-maxnorm-function/) 函数
*   TF。约束。限制类[。约束。最小最大范数()](https://www.geeksforgeeks.org/tensorflow-js-tf-constraints-minmaxnorm-function/)函数
*   tf .约束类 [.constraints.nonNeg()](https://www.geeksforgeeks.org/tensorflow-js-tf-constraints-nonneg-function/) 函数
*   TF。约束。限制类[。约束。unitnorm()](https://www.geeksforgeeks.org/tensorflow-js-tf-constraints-unitnorm-function/)

**示例 1:** 在本例中，**TF . constraints . constraints class . constraints . minmax norm()函数**用于基于给定的配置对象创建 *minMaxNorm* 约束。它继承自约束类。约束是层的属性，如权重、核、偏差。 *minMaxNorm* 是一个重量约束。

## JavaScript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Calling maxNorm() function
var a = tf.constraints.maxNorm(2, 0)

// Printing output
console.log(a)
```