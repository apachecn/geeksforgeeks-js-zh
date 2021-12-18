# tensorlow . js TF . depthtospace()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-depthtospace-function/

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf.depthToSpace() i** 是 **tensorflow.js** 库的内置函数，用于重新排列输入张量中的数据，其中深度维度的值在空间块中移动到高度和宽度维度。它将数据从深度重新排列成空间数据块。

**语法:**

```
tensor.depthToSpace(input, blocksize, dataformat)
```

**参数:**

*   **输入:**给定张量
*   **块大小:**输出张量的宽度为深度*块大小。
*   **数据格式**:指定给定和结果张量的布局。它有两个选项:“NHWC”:[批次、高度、宽度、通道]和“NCHW”:[批次、通道、高度、宽度]

**返回值:**返回相同数据类型的重排张量。

**示例 1:** 使用**【NHWC】格式**

## **java 描述语言**

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Create a new tensor
var input = tf.tensor4d([1, 3, 5, 7], [1, 1, 1, 4]);

// define block size
var blockSize = 2;

// define data format
var dataFormat = "NHWC";

// rearrange data
var val = tf.depthToSpace(input, blockSize, dataFormat);

// print the tensor
val.print();
```

****输出:****

```
Tensor
    [[[[1],
       [3]],

      [[5],
       [7]]]]
```

****示例 2:** 使用“NCHW”格式**

## **java 描述语言**

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Create a new tensor
var input = tf.tensor4d([1, 3, 5, 7], [1, 4, 1, 1]);

// define block size
var blockSize = 2;

// define data format
var dataFormat = "NCHW";

// rearrange data
var tr = tf.depthToSpace(input, blockSize, dataFormat);

// print the tensor
tr.print();
```

 ****输出:****

```
Tensor
    [[[[1, 3],
       [5, 7]]]]
```

****参考:**T2】https://js.tensorflow.org/api/latest/#depthToSpace**