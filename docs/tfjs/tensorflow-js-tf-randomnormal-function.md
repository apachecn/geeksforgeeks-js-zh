# tensorlow . js TF . random shape()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-random formal-function/

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它帮助开发人员在 JavaScript 中开发 ML 模型，并直接在浏览器或 Node.js 中使用 ML。

**tf.randomNormal()函数**用于创建一个 tf。从正态分布中取样的张量。

**语法:**

```
tf.randomNormal (shape, mean, stdDev, dtype, seed)
```

**参数:**

*   **形状:**定义输出张量形状的整数数组。
*   **的意思是:**是可选参数。正态分布的平均值。
*   **stdDev:** 也是可选参数。正态分布的标准差。
*   **数据类型:**输出的数据类型。可能的数据类型值是“float32”或“int32”。这也是一个可选的参数。
*   **seed:** 是可选参数。随机数生成器的种子。

**返回值:**返回 tf.Tensor

**例 1:**

## Javascript

```
// Creating the tensor with values 
// sampled from a normal distribution
const x = tf.randomNormal([5]);

// Printing the tensor
x.print();
```

**输出:**

```
Tensor
   [1.5322036, 2.2685387, -0.4921667, 1.1309422, 1.470457]
```

**例二:**

## Javascript

```
// Creating the tensor with values 
// sampled from a normal distribution
const x = tf.randomNormal([2, 2]);

// Printing the tensor
x.print();
```

**输出:**

```
Tensor
   [[1.9162624 , -0.9760998],
    [-0.2262698, -2.1717837]]
```

**例 3**

## Javascript

```
// Creating the tensor with values 
// sampled from a normal distribution
const x=tf.randomNormal([5], 5, 1, 'int32', 2);

// Printing the tensor
x.print();
```

**输出:**

```
​Tensor
   [5, 7, 6, 5, 6]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#randomNormal