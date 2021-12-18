# tensorflow . js TF . signal . frame()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-signal-frame-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-signal-frame-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf.signal.frame()** 函数用于将输入扩展为帧长的帧。

**语法:**

```
tf.signal.frame (signal, frameLength, frameStep, 
                      padEnd?, padValue?)
```

**参数:**

*   **信号:**待展开的输入张量。
*   **帧长:**帧的长度
*   **帧步长:**样本中的帧跳跃大小
*   **padEnd:** 是否用 padValue 填充信号结束。
*   **padValue:** 当 padEnd 为真时，输入信号不存在时使用的数字。

**返回值:**返回 tf.Tensor

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

tf.signal.frame([1, 2, 3, 4, 5, 6], 2, 3).print();
```

**输出:**

```
Tensor
     [undefined,]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

tf.signal.frame([2,, 4, 6], 1, 3).print();
```

**输出:**

```
Tensor
     [undefined,]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#signal.frame