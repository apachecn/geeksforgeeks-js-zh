# tensorlow . js TF . note qual()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-notqual-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**TF . noteqal()**函数用于返回布尔值张量，即如果第一个张量的值不等于第二个张量的值，则返回真，否则返回假。它支持广播。

**语法:**

```
tf.notEqual(a, b)
```

**参数:**该函数接受两个参数，如下图所示:

*   **a:** 第一个输入张量。
*   **b:** 第二个输入张量。它应该具有与“a”相同的数据类型。

**返回值:**它返回一个布尔值张量，即如果第一个张量的值不等于第二个张量的值，则返回真，否则返回假。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing some tensors
const a = tf.tensor1d([1, 2, 3, 4]);
const b = tf.tensor1d([1, 4, 3, 4]);

// Calling the .notEqual() function
a.notEqual(b).print();
```

**输出:**

```
Tensor
   [false, true, false, false]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using tensors of some values as
// the parameters of .notEqual() function
tf.tensor1d([0.1, 2.06, 2.1, 3.0]).notEqual(
tf.tensor1d([.1, 2.6, 2.0, 3])).print();
```

**输出:**

```
Tensor
   [false, true, true, false]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#notEqual