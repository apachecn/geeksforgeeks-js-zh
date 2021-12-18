# Tensorflow.js tf.moments()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-moments-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-moments-function/)

**tf.moments()** 用于计算在函数中作为参数传递的张量的均值和方差。平均值和方差是通过聚集参数传递的轴上张量的内容来计算的。

**语法:**

```
tf.moments(tensor, axis, keepdims)
```

**参数:**该方法接受以下三个参数:

*   **Tensor:** Tensor (vector) for which the mean and variance need to be calculated.
*   **Axis:** An integer vector representing the axis for which the mean value and variance need to be calculated.
*   [t0 T0】 keepdims: keepdims is a Boolean variable that indicates whether the generated moment has the same dimension as the input tensor.

**返回值:**它返回两个张量对象，即计算的平均值和方差。

**示例 1:** 在本例中，我们将计算一维张量的真实均值和方差。

## Javascript

```
// Creating 1-D Tensor
const tensor = tf.tensor1d([1, 2, 3, 4, 5, 6, 7, 8, 9]);

// Calculating mean and Variance using tf.moments()
const value = tf.moments(tensor,[0]);

// Printing mean and variance
console.log("Mean: ",value.mean,"\nVariance: ",value.variance);
```

**输出:**

```
Mean:  Tensor
    5 
Variance:  Tensor
    6.666666507720947
```

**示例 2:** 在本例中，我们将计算二维张量均值和方差的浮点值。

## Javascript

```
// Creating 2-D Tensor
tensor = tf.tensor2d([[1,2,4],[3,7,4],[7,5,1]])

// Calculating mean and Variance using tf.moments()
value = tf.moments(tensor,axes=[0])

// Printing mean and variance
console.log("Mean: ",value.mean,"\nVariance: ",value.variance);
```

**输出:**

```
Mean:  Tensor
    [3.6666667, 4.666667, 3] 
Variance:  Tensor
    [6.2222228, 4.2222223, 2]
```

**示例 3:** 在上面的示例中，平均值和方差是跨轴[0]计算的，即[(1+3+7)/3，(2+7+5)/3，(4+4+1)/3]，在此示例中，我们将参数轴设置为[1]。

## Javascript

```
// Creating 1-D Tensor
tensor = tf.tensor2d([[3,2,4],[3,7,4],[7,5,1]]);

// Calculating mean and Variance using tf.moments() across axis=[1]
value = tf.moments(tensor,axes=[1])

// Printing mean and variance
console.log("Mean: ",value.mean,"\nVariance: ",value.variance);
```

**输出:**平均值计算为[(3+2+4)/3，(3+7+4)/3，(7+5+1)/3]

```
Mean:  Tensor
    [3, 4.666667, 4.3333335] 
Variance:  Tensor
    [0.6666667, 2.8888888, 6.2222228]
```

**例 4:** 在本例中，我们将通过改变轴=[0，1]来计算完整向量的均值和方差。

## Javascript

```
// Creating 2-D Tensor
tensor = tf.tensor2d([[3,2,4],[3,7,4],[7,5,1]])

// Calculating mean and Variance using tf.moments()
value = tf.moments(tensor,[0,1])

// Printing mean and variance
console.log("Mean: ",value.mean,"\nVariance: ",value.variance);
```

**输出:**

```
Mean:  Tensor
    4 
Variance:  Tensor
    3.777777910232544
```

**注:**计算均值和方差是张量的归一化。*****TF . nn . moments()***在 JavaScript 中可以很好地工作，但是如果我们在 python 中导入 TensorFlow 模块，我们将使用***TF . nn . moments()***来执行相同的操作。**