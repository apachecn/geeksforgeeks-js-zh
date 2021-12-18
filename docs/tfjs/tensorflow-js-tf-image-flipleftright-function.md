# tensorlow . js TF . image . flippeleftriht()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-image-flippetriht-function/

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**.image.flipLeftRight()功能**用于将所述图像从左手侧翻转到右手侧。目前它可以在*中央处理器*、*网易*以及 *WASM* 后台访问。

**语法:**

```
tf.image.flipLeftRight(image)
```

**参数:**

*   **图像:**是所述的结构 4d 张量[批次，图像高度，图像宽度，深度]。它可以是 tf 类型。张量 4D、TypedArray 或数组。

**返回值:**返回 tf。张量 4D 对象。

**示例 1:** 在本例中，我们将看到在 tensorflow . js TF . image . flipleftright()函数中使用 4d 张量的用法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling image.flipLeftRight() method and
// Printing output
tf.image.flipLeftRight(tf.tensor4d([[

  [[4, 7], [21, 9]],

  [[8, 9], [1, 5]]

]])).print();
```

**输出:**

```
Tensor
    [[[[21, 9],
       [4 , 7]],

      [[1 , 5],
       [8 , 9]]]]
```

**示例 2:** 在本例中，我们将看到在 tensorflow . js TF . image . flipleftright()函数中使用一个浮点数组。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining an array of floats
const arr = [[

  [[1.1, 1.7, 1.5, 1.1], 
  [1.7, 1.9, 8.1, 6.3]],
  [[3.3, 3.4, 3.7, 4.0], 
  [5.1, 5.2, 5.3, 5.9]]

]];

// Calling image.flipLeftRight() method and
// Printing output
tf.image.flipLeftRight(arr).print();
```

**输出:**

```
Tensor
    [[[[1.7      , 1.9      , 8.1000004, 6.3000002],
       [1.1      , 1.7      , 1.5      , 1.1      ]],

      [[5.0999999, 5.1999998, 5.3000002, 5.9000001],
       [3.3      , 3.4000001, 3.7      , 4        ]]]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#image.flipLeftRight