# tensorlow . js TF . bincount()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-bincount-function/

**简介:** Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型以及深度学习神经网络。函数的作用是:用相同的数据类型生成所提供大小的张量。张量的值将是所提供的权重张量的索引处的数的和，该索引对应于输入张量中索引数的索引。

**语法:**

```
tf.bincount( x ,weights ,size )
```

**参数:**

*   **X:** The variable is the input tensor. It should be a one-dimensional tensor.
*   **Weight:** The variable is a tensor with the same size as x. It is a value corresponding to the value in the x tensor.
*   **Size:** The state value is the size of the output tensor.

**返回:** tf.tensor1D

#### **TF . bin count()函数基本示例:**

**示例 1:** 在这个示例中，我们创建一个张量，并计算大小之间的数字的出现次数，然后将其打印出来。

## Javascript

```
// Importing tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing the input
const geek_input = tf.tensor([1, 2, 9, 6, 5, 4, 7,
    4, 7, 4, 3, 2, 4, 2, 5, 1], [1, 16], 'int32');

// Printing Input tensor
console.log('Input tensor: ',geek_input)

// Weight and size  for the bincount
const geek_Weight = [];
const geek_size = 5;

// Applying bincount to input tensor
const r = tf.bincount(geek_input, geek_Weight,geek_size)

// Printing result
console.log("Number of Index Number in tensor: ",r)

// Printing Occurrence of index in tensor
const r1 = r.arraySync();
r1.map((e,i) => {console.log(`Index ${i} occures`, e ,"times")})
```

**输出:**

```
Input tensor:  Tensor
     [[1, 2, 9, 6, 5, 4, 7, 4, 7, 4, 3, 2, 4, 2, 5, 1],]

Number of Index Number in tensor:  
Tensor
    [0, 2, 3, 1, 4]

Index 0 occures 0 times
Index 1 occures 2 times
Index 2 occures 3 times
Index 3 occures 1 times
Index 4 occures 4 times
```

**示例 2:** 在本例中，我们创建了一个输入张量和权重张量，并将其传递给 bincount 函数，看看 bincount 如何计算输出张量的值。

## Javascript

```
// Importing tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing the input
const geek_input = tf.tensor([1, 2, 9, 6, 5,
    4, 7, 4, 7, 4, 3], [1, 11], 'int32');

// Printing Input tensor
console.log('Input tensor: ',geek_input)

// Weight and size  for the bincount
const geek_Weight = tf.tensor(
    [0, 2, 5, 8, 9, 3, 5, 5, 3, 8, 2]);

const geek_size = 8;

// Applying bincount to input tensor
const r = tf.bincount(geek_input,geek_Weight,geek_size)

// Printing result
console.log("Output tensor: ",r)
```

**输出:**

```
Input tensor:  Tensor
     [[1, 2, 9, 6, 5, 4, 7, 4, 7, 4, 3],]
Output tensor:  Tensor
    [0, 0, 2, 2, 16, 9, 8, 8]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#bincount