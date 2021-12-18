# tensorflow . js TF . local response normalization()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-locaresponsenormalization-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-localresponsenormalization-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。localResponseNormalization()函数**用于标准化通过通道或通道内部与局部邻域相连的刺激。

**语法:**

```
tf.localResponseNormalization (x, depthRadius?, bias?, alpha?, beta?)
```

**参数:**

*   **x:** 是所述的输入张量。其中，4D 输入张量被认为是一个参考 1D 向量的三维数组，具有最大的尺寸。此外，每个向量都被单独标准化。它可以是 tf 类型。张量 3D，tf。张量 4D、TypedArray 或数组。
*   **depthRadius:** 是 1D 窗口标准化中并列通道的规定计数。它是可选的，并且是数字类型。
*   **偏差:**是碱基恒定的偏差表达式。它是可选的，并且是数字类型。
*   **α:**一般来说，规定的比例因子是正的。它是可选的，并且是数字类型。
*   **β:**是可选的规定指数，类型号。

**返回值:**返回 tf。张量 3D，或 tf .张量 4D。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tf.tensor3d input
const x = tf.tensor3d([1, 2, 3, 4, 6, 6], [1, 2, 3]);

// Calling tf.localResponseNormalization() method
// and printing output
x.localResponseNormalization().print();
```

**输出:**

```
Tensor
    [[[0.2581989, 0.5163978, 0.7745967],
      [0.4239992, 0.6359987, 0.6359987]]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
// import * as tf from "@tensorflow/tfjs"

// Calling tf.localResponseNormalization() method
// and printing output
tf.localResponseNormalization(
    tf.tensor3d([1.1, 3.2, -3, null, 5, 0], 
    [1, 1, 6]), 4, 3, 2, 1).print();  
```

**输出:**

```
Tensor
     [ [[0.0117146, 0.0340788, -0.0319489, 0, 0.0532481, 0],]]
```

**参考:**[https://js . tensorflow . org/API/latest/# localhostionalization](https://js.tensorflow.org/api/latest/#localResponseNormalization)