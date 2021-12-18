# tensorlow . js TF . logicaland()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-logicaland-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.logicalAnd()** 函数用于为两个指定的布尔值张量的元素式“与”运算结果返回一个布尔值张量。

**语法:**

```
tf.logicalAnd(a, b)
```

**参数:**该函数接受两个参数，如下图所示:

*   **a:** 第一个输入张量。它应该具有布尔数据类型。
*   **b:** 第二个输入张量。它应该具有布尔数据类型。

**返回值:**返回两个指定的布尔值张量按元素与运算的结果的布尔值张量。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing two different tensors of Boolean values
const a = tf.tensor1d([true, false, false, true], 'bool');
const b = tf.tensor1d([false, false, true, true], 'bool');

// Calling the .logicalAnd() function
a.logicalAnd(b).print();
```

**输出:**

```
Tensor
   [false, false, false, true]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using two different tensors of Boolean values
// as the parameters of .logicalAnd() function
tf.tensor1d([true, true, false, true], 'bool').
logicalAnd(tf.tensor1d([true, false, false, true], 
           'bool')).print();
```

**输出:**

```
Tensor
    [true, false, false, true]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#logicalAnd