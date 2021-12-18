# tensorflow . js . TF . loss . sigmoidcross 熵()函数

> 原文:[https://www . geeksforgeeks . org/tensorflow-js-TF-loss-sigmoidcross 熵-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-losses-sigmoidcrossentropy-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

函数计算两个给定张量之间的 sigmoid 交叉熵损失。

**语法:**

```
tf.losses.sigmoidCrossEntropy(
    multiClassLabels, logits, weights, 
    labelSmoothing, reduction
); 
```

**参数:**

*   **multiClassLabels:** 是 num 类、批量大小等不同形状的地面真值输出张量。它在维度上与*的预测*相似。
*   **逻辑:**预测的是输出。
*   **重量:**这些是等级不是 0 就是 1 的张量，必须是宽可铸到勒贝尔。
*   **labelSmoothing:** 如果该值大于 0，则表示将平滑标签。
*   **还原:**适用于亏损的还原类型。它必须是缩减类型。

**注意:***重量*、*标签重量*和*减少量*为可选参数。

**返回值:**返回 tf.Tensor。

**例 1:**

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Initialising tensor1 as geek1.
let geek1 = tf.tensor3d([[[1], [2]], [[3], [4]]]);

// Initialising tensor2 as geek2.
let geek2 = tf.tensor3d([7, 11, 13, 4], [2, 2, 1])

// Computing sigmoid Cross Entropy loss
// between geek1 and geek2
// using .sigmoidCrossEntropy) function.
geek = tf.losses.sigmoidCrossEntropy(geek1, geek2)
geek.print();
```

**输出:**

```
Tensor
    -12.245229721069336
```

**例二:**

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Computing sigmoid Cross Entropy loss
// between two 4D tensors and
// printing the result.
tf.losses.sigmoidCrossEntropy(
    tf.tensor4d([[[[9], [8]], [[7], [5]]]]),
    tf.tensor4d([[[[1], [2]], [[3], [4]]]])
).print();
```

**输出:**

```
Tensor
    -13.873268127441406
```

**参考:**[**https://js . tensorflow . org/API/latest/# loss . sigmoidcross 熵**](https://js.tensorflow.org/api/latest/#losses.sigmoidCrossEntropy)