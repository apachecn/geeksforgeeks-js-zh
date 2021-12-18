# tensorlow . js TF .混淆矩阵()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-confusion matrix-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。混淆矩阵()函数**用于根据所述真实标签和预测标签计算混淆矩阵。

**语法:**

```
tf.confusionMatrix(labels, predictions, numClasses)
```

**参数:**

*   **标签:**指定的目标标签应该是有利于类的基于零的整数。它有形状[numExamples]。其中， *numExamples* 是合并实例的度量。它可以是 tf 类型。张量 1D、TypedArray 或数组。
*   **预测:**所述的预测类应该是有利于类的基于零的整数。它应该具有与所述标签相当的形状。它可以是 tf 类型。张量 1D、TypedArray 或数组。
*   **numClasses:** 是整数类型的总类数。此外，它的度量应该大于所述标签和预测中最大的元素。它是数字类型的。

**返回值:**返回 tf。张量 2D 对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining predictions, labels and 
// numClasses
const lab = tf.tensor1d([3, 4, 1, 0, 1], 'int32');
const pred = tf.tensor1d([1, 3, 0, 4, 1], 'int32');
const num_Cls = 2;

// Calling tf.confusionMatrix() method
const output = tf.math.confusionMatrix(lab, pred, num_Cls);

// Printing output
output.print();
```

**输出:**

```
Tensor
    [[0, 0],
     [1, 1]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling tf.confusionMatrix() method
const res = tf.math.confusionMatrix(
    tf.tensor1d([3.3, 4.5, null, 'a', 'b']), 
    tf.tensor1d([-2, 5.3, -0.1, 4.3, 12.5]), 4
);

// Printing output
res.print();
```

**输出:**

```
Tensor
    [[1, 0, 0, 0],
     [0, 0, 0, 0],
     [0, 0, 0, 0],
     [0, 0, 0, 0]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#confusionMatrix