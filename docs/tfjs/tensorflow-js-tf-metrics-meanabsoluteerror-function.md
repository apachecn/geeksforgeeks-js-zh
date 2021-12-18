# tensorlow . js TF . metrics . meanabsolute error()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-metrics-meanabsolute error-function/

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

用于计算平均绝对误差。平均绝对误差定义为两个张量绝对差的平均值。其中，平均值应用于特征尺寸。它以两个张量为参数。

```
mean(abs(Prediction - True))
```

**语法:**

```
tf.metrics.meanAbsoluteError(Tensor1, Tensor2);
```

**参数:**

*   **张量 1:** 是真张量。
*   **张量 2:** 是预测张量。

**返回值:**返回平均绝对误差的张量。

**例 1:** 在这个例子中，我们给出了两个一维张量作为参数，metrics.meanAbsoluteError 函数将计算平均绝对误差并返回一个张量。

## Javascript

```
// Importing the tensorflow library
import * as tf from "@tensorflow/tfjs"

// Defining the value of the tensors
const True = tf.tensor([1,2,3]);
const Prediction = tf.tensor([3,2,1]);

// Calculating mean absolute error
const error = tf.metrics.meanAbsoluteError(True, Prediction);

// Printing the tensor
error.print();
```

**输出:**

```
Tensor
    1.3333333730697632
```

**示例 2:** 在这个示例中，我们给出了两个 2d 张量作为参数，metrics.meanAbsoluteError 函数将计算平均绝对误差并返回一个张量。

## Javascript

```
// Importing the tensorflow library
import * as tf from "@tensorflow/tfjs"

// Defining the value of the tensors
const True = tf.tensor([[1,2,3],[2,4,1]]);
const Prediction = tf.tensor([[3,2,1],[5,2,1]]);

// Calculating mean absolute error
const error = tf.metrics.meanAbsoluteError(True, Prediction);

// Printing the tensor
error.print();
```

**输出:**

```
Tensor
    [1.3333334, 1.6666667]
```

**参考:**[https://js . tensorflow . org/API/latest/# metrics . mean absolutherror](https://js.tensorflow.org/api/latest/#metrics.meanAbsoluteError)