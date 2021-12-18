# tensorlow . js TF . conv 3d()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-conv 3d-function/

**Tensorflow.js** 是谷歌开发的 javascript 库，用于在浏览器或 Node.js 中运行和训练机器学习模型。

**tf.conv3d()** 函数用于计算给定输入上的 3d 卷积。输入主要是 3D 图像数据，如计算机断层扫描或核磁共振成像或任何视频。为了从这些数据中提取特征，我们使用一个卷积层来创建卷积核，并输出 4D 或 5D 张量。

**语法:**

```
tf.conv3d (x, filter, strides, pad, dataFormat?, dilations?) 
```

**参数:**

*   **x**:4 和 5 的张量秩被送入卷积。张量也可以是具有形状[批次、深度、高度、宽度、通道]的类型化数组。
*   **过滤器**:过滤器等级为 5，数据类型与 x 相同，形状为【过滤器深度、过滤器高度、过滤器宽度、通道内、通道外】。过滤器和输入的 inchannels 必须匹配。
*   **步幅:**步幅用于在输入张量上移动过滤器。为此，传递了一个长度为> =5 的列表。
*   **填充:**填充算法属于“相同”和“有效”类型。“相同”将创建与输入大小相同的输出。而“有效”输出将比输入小。
*   **数据格式**:在两个字符串中，可以是“NHWC”、“NCHW”。默认格式为“NHWC”，数据按以下顺序存储:[批次、深度、高度、宽度、通道]。需要指定输入和输出数据的数据格式。这是可选的。
*   **膨胀**:膨胀率是检查卷积率的两个整数元组。[扩展深度，扩展高度，扩展宽度]作为参数传递。这是可选的。

**示例 1:** 在本例中，我们将手动创建输入和核张量，并执行卷积运算。我们将打印出张量的形状，以记录通道数和填充算法。

## Javascript

```
// Importing libraries
import * as from "@tensorflow/tfjs"

// Input tensor
const X=tf.tensor5d([[[[[0.],[2.]],
                       [[3.],[1.]],
                       [[4.],[2.]]],
                      [[[1.],[0.]],
                       [[2.],[1.]],
                       [[4.],[2.]]]]]);
console.log('Shape of the input:' ,X.shape);

// Kernel vector has been set
const kernel=tf.tensor5d([[[[[0.3,1.2]]],[[[0.6,1.8]]],[[[0.8,1.5]]]]]);
console.log('Shape of the kernel:' ,kernel.shape);

// Output tensor after convolution
let output=tf.conv3d(X,kernel,strides=[1,1,1,1,1],'same');
output.print();
console.log('Shape of the output tensor:',output.shape);
```

**输出:**

```
Shape of the input: 1,2,3,2,1
Shape of the kernel: 1,3,1,1,2
Tensor
    [[[ [[2        , 5.0999999],],

        [[2.8000002, 7.1999998],],

        [[1.5      , 4.8000002],]],

      [ [[0.8      , 1.5      ],],

        [[2.2      , 4.8000002],],

        [[1.5      , 4.8000002],]]]]
Shape of the output tensor: 1,2,3,1,2
```

**示例 2:** 在下面的代码中，由于 inchannels 数(即输入张量的第五个索引和核张量的第四个索引)不匹配，将会出现错误。

## Javascript

```
import * as from "@tensorflow/tfjs"

// Input tensor
const X=tf.tensor5d([0.,2.,3.,1.,4.,2.,1.,0.,2.,1.,4.,2.],[1,2,3,2,1]);

// Kernel vector has been set
const kernel=tf.tensor5d([0.3,1.2,0.6,1.8,0.8,1.5],[1,1,1,2,3]);

// Output tensor after convolution
let output=tf.conv3d(X,kernel,strides=[1,1,1,2,1],'same');
output.print();
console.log('Shape of the output tensor:',output.shape);
```

**输出:**

```
An error occured on line: 10
Error in conv3d: depth of input (1) must match input depth for filter 2.
```

**示例 3:** 在本例中，我们将执行两个卷积运算。首先，我们将创建一个从正态分布中随机选取的值的张量，并在卷积后打印输出张量。之后，我们取一个更大尺寸的张量(可以是 3D 图像或视频)，并执行卷积，这将再次生成一个大张量。我们将打印该张量的输出形状。

## Javascript

```
// Importing libraries
import * as from "@tensorflow/tfjs"

// A tensor with values selected from a
// normal distribution
const x=tf.randomNormal([1,2,4,1,3]);

const kernel=tf.tensor5d([0.3,1.2,0.6,1.8,0.8,1.5],[1,1,2,3,1])

// Output tensor after convolution
let out=tf.conv3d(x,kernel,strides=[1,1,1,1,1],'same')

// Printing the output tensor
console.log('First output tensor is:')
out.print()

// Input tensor of bigger shape is taken
const y=tf.randomNormal([3,25,25,25,1]);

const kernel2=tf.randomNormal([1,3,3,1,1])

// Convolution is performed
let output2=tf.conv3d(y,kernel2,strides=[1,1,1,1,1],'same')

// Output2.print()
// Printing out the bigger output shape
console.log('\n The shape of the output tensor',output2.shape)
```

**输出:**

```
First output tensor is:
Tensor
    [[[ [[-0.702378 ],],

        [[1.9029824 ],],

        [[-0.1904218],],

        [[-2.2287691],]],

      [ [[-1.9580686],],

        [[-2.8335922],],

        [[0.0155853 ],],

        [[-3.6478395],]]]]

 The shape of the bigger output tensor 3,25,25,25,1
```

**参考资料:**[https://js . tensorlow . org/API/1 . 0 . 0/# conv 3d](https://js.tensorflow.org/api/1.0.0/#conv3d)