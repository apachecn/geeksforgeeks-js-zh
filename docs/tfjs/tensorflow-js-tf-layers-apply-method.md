# tensorflow . js . TF . layers apply()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-apply-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-apply-method/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**tf.layers apply()方法**用于执行 layers 计算，并在我们用 tf 调用它时返回 Tensor。张量。如果我们叫它 tf。然后，符号传感器将为将来的执行准备层。

**语法:**

```
apply (inputs, kwargs)
```

**参数:**

*   **输入:**此参数将数组保存为输入。
*   **kwargs[Optional]:** 它是一个可选参数，保存要传递给 call()的附加关键字参数。

**返回值:**返回同一数据类型的张量或符号传感器。

下面的例子说明了 Tensorflow.js tf.layers apply()方法:

**例 1:**

## Javascript

```
import * as tf from "@tensorflow/tfjs"

const denseLayer = tf.layers.dense({
   units: 1,
   kernelInitializer: 'ones',
   useBias: false
});

const input = tf.ones([2, 2]);
const output = denseLayer.apply(input);

// Print the output
print(output)
```

**输出:**

```
Tensor [[2], [2]]
```

**例二:**

## Javascript

```
import * as tf from "@tensorflow/tfjs"

const denseLayer = tf.layers.dense({
   units: 1,
   kernelInitializer: 'zeros',
   useBias: false
});

const input = tf.ones([2, 2]);
const output = denseLayer.apply(input);

// Print the output
print(output)
```

**输出:**

```
Tensor [[0], [0]]
```

**参考:**T2**https://js.tensorflow.org/api/latest/#tf.layers.Layer.apply**T5】