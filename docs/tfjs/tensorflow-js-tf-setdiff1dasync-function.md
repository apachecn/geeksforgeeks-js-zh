# tensorlow . js TF . setdiff 1 das sync()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-setdiff 1 das sync-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.setdiff1dAsync()** 函数用于查找两个指定数字列表之间的差异。

让我们假设给定了两个张量“a”和“b”，然后这个函数返回一个张量 out，它代表“a”中存在但“b”中不存在的所有值。返回的张量按照表示“a”的相同顺序进行排序。该函数还返回张量输出中的指数张量。

**语法:**

```
tf.setdiff1dAsync (a, b)
```

**参数:**这个函数接受两个参数，如下图所示:

*   **A:** It is a one-dimensional tensor value to be maintained.
*   **B:** It is the one-dimensional tensor value to be excluded from the output. It should have the same data type as "A".

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing two Tensors
const a = [10, 20, 30, 40, 50, 60];
const b = [20, 40, 50];

// Calling the .setdiff1dAsync() function over
// the above two specified Tensors as parameters
// and returns the Tensor out and indices for
// the same
const [out, indices] = await tf.setdiff1dAsync(a, b);

// Getting the Tensor of values present in
// Tensor "a" but not in "b"
out.print();

// Getting the Tensor of indices for the
// returned Tensor's values
indices.print();
```

**输出:**

```
Tensor
   [10, 30, 60]
Tensor
   [0, 2, 5]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using two Tensors as the parameters for the
// .setdiff1dAsync() function and
// returns the Tensor out and indices
const [out, indices] = await
  tf.setdiff1dAsync([0.1, 0, 7.0, 7.1], [.1, 7]);

// Getting the Tensor of values present in
// Tensor first Tensor parameter
// but not in second one
out.print();

// Getting the Tensor of indices for the
// returned Tensor's values
indices.print();
```

**输出:**

```
Tensor
   [0, 7.0999999]
Tensor
   [1, 3]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#setdiff1dAsync