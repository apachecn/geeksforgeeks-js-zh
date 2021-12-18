# tensorflow . js TF . data . dataset 类。批次()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-dataset-class-batch-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-dataset-class-batch-method/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf.data.Dataset.batch()** 函数用于将元素分组为批次。

**语法:**

```
tf.data.Dataset.batch(batchSize, smallLastBatch?)
```

**参数:**

*   **批次大小:**单个批次中应该存在的元素。
*   **smalllastpatch:**如果为真，则如果最终批次的元素少于 batchSize，则最终批次将发出元素，反之亦然。默认值为真。提供此值是可选的。

**返回值:**返回一个 tf.data.Dataset。

**示例 1:** 在本例中，我们将取一个大小为 6 的数组，并将其分成多个批次，每个批次有 3 个元素。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating an array
const gfg = tf.data.array(
  [10, 20, 30, 40, 50, 60]
).batch(3);

// Printing the elements
await gfg.forEachAsync(
  element => element.print()
);
```

**输出:**

```
"Tensor
    [10, 20, 30]"
"Tensor
    [40, 50, 60]"
```

**例 2:** 这次我们取 8 个元素，试着分批拆分，每个元素 3 个。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating an array
const gfg = tf.data.array(
  [10, 20, 30, 40, 50, 60, 70, 80]
).batch(3);

// Printing the elements
await gfg.forEachAsync(
  element => element.print()
);
```

**输出:**

```
"Tensor
    [10, 20, 30]"
"Tensor
    [40, 50, 60]"
"Tensor
    [70, 80]"
```

由于默认情况下 smallLastBatch 的默认值为真，因此我们看到第三批包含 2 个元素。

**示例 3:** 这次我们将 smallLastBatch 参数作为 false 传递。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating an array
const gfg = tf.data.array(
  [10, 20, 30, 40, 50, 60, 70, 80]
).batch(3, false);

// Printing the elements
await gfg.forEachAsync(
  element => element.print()
);
```

**输出:**

```
"Tensor
    [10, 20, 30]"
"Tensor
    [40, 50, 60]"
```

由于 smallLastBatch 的默认值为 false，我们看不到第三批，因为最后一批中只有 2 个元素小于 3，即指定的批大小。

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.data.Dataset.batch