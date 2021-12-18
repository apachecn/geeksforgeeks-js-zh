# tensorlow . js TF . clippbyvalue()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-clippbyvalue-function/

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。clipByValue()函数**用于查找所述张量输入的剪辑值，并且是按元素进行的。

**语法:**

```
tf.clipByValue(x, clipValueMin, clipValueMax)
```

**参数:**

*   **x:** 它是张量输入，其值将被剪切，并且它可以是类型 *tf。张量*，或*型达瑞*，或*阵列*。
*   **裁剪值最小值:**是要裁剪的指定范围的下限。
*   **裁剪值最大值:**是要裁剪的指定范围的上限。

**返回值:**返回 tf。张量对象。

**示例 1:** 在这个示例中，我们定义了一个整数类型的输入张量，然后打印它的裁剪值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([9, -10, -19, 12]);

// Calling clipByValue() method and
// printing output
y.clipByValue(-11, 11).print();
```

**输出:**

```
Tensor
    [9, -10, -11, 11]
```

**示例 2:** 在本例中，浮点类型值被视为张量输入，所有参数都直接传递给 *clipByValue* 函数。

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [.5, 4.9, .275, -1.46];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling clipByValue() method
var res = tf.clipByValue(y, -1, 1);

// printing output
res.print();
```

**输出:**

```
Tensor
    [0.5, 1, 0.275, -1]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#clipByValue