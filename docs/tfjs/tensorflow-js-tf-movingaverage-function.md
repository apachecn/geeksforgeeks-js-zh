# tensorflow . js TF . movingaverage()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-movingaverage-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-movingaverage-function/)

**简介:** Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型以及深度学习神经网络。

**。movingAverage()函数**用于确定一个变量的移动平均值。

**注:**

*   Without *zerodebias* , the moving average operation is specified as: v += delta. Where δ = (1–attenuation) * (x–v).
*   In the presence of *zero debias* (default value), measure the delta term to remove the influence of (assumed) zero initialization of V, where delta/=(1- attenuation step size).
*   This function is completely stateless and does not keep the step path. In addition, the number of steps is required to be saved by the caller and passed in as *step* .

**语法:**

```
tf.movingAverage(v, x, decay, step?, zeroDebias?)
```

**参数:**

*   **V:** The current moving average. It can be tf type. Tensor, type or array.
*   **X: the new input value described in** , which should have the same shape and data type, such as *V* .
*   **Decay: the decay factor specified in** . The values are usually 0.95 and 0.99\. It can be a type number, or tf.Scalar 。
*   **Step: the number of steps described in** . It is optional and is of type number or tf.scalar. 。
*   **zerodebias:** It checks whether to execute *zerodebias* . The default value is true. Optional, the type is *Boolean* .

**返回值:**返回 tf.Tensor

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining current moving average value
const v = tf.tensor1d([1, 3, 5, 1]);

// Defining new input value
const x = tf.tensor1d([1, 7, 2, 1]);

// Defining decay factor
const decay_factor = 0.75;

// Calling movingAverage() method
const res = tf.movingAverage(v, x, decay_factor, 2, true);

// Printing output
res.print();
```

**输出:**

```
Tensor
    [1, 5.2857141, 3.2857144, 1]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling movingAverage() method
tf.movingAverage(tf.tensor1d([1.1, 3.1, 5.5, 1.3]),
               tf.tensor1d([1.2, 7.4, 2.6, 1.1]), 0.99, 5, false).print();
```

**输出:**

```
Tensor
    [1.1010001, 3.1429999, 5.4710002, 1.298]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#movingAverage