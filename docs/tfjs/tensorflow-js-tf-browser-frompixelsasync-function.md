# tensorflow . js TF . browser . from pixelsasync()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-browser-from pixelsasync-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-browser-frompixelsasync-function/)

[**Tensorflow.js**](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**函数用于以异步方式创建指定图像的像素值张量。**

**语法:**

```
tf.browser.fromPixelsAsync (pixels, numChannels)
```

**参数:**该函数接受两个参数，如下图所示。

*   **像素:**它是输入图像的像素，张量将从这些像素中构建。支持的图像类型都是 4 通道。
*   **numchannels:** 是输出 Tensor 的通道数。它的默认值是 3，上限是 4。

**返回值:**该函数返回指定图像的像素值的创建张量。

**例 1:**

## java 描述语言

```
// Creating a image from some specified
// pixels values
const image = new ImageData(2, 2);
image.data[0] = 5;
image.data[1] = 10;
image.data[2] = 15;
image.data[3] = 20;

// Calling the .fromPixelsAsync() function
// over the above image as its parameter
// without using numChannels value so
// it print only 3 pixels value as
// the default value of numchannels
// parameter is 3
(await tf.browser.fromPixelsAsync(image)).print();
```

**输出:**

```
Tensor
   [[[5, 10, 15],
     [0, 0 , 0 ]],

    [[0, 0 , 0 ],
     [0, 0 , 0 ]]]
```

**例 2:**

## java 描述语言

```
// Creating a image from some specified
// pixels values
const image = new ImageData(1, 1);
image.data[0] = 5;
image.data[1] = 10;
image.data[2] = 15;
image.data[3] = 20;

// Calling the .fromPixelsAsync() function
// over the above image as its parameter
// along with 4 value for numChannels parameter
(await tf.browser.fromPixelsAsync(image, 4)).print();
```

**输出:**

```
Tensor
    [ [[5, 10, 15, 20],]]
```

**参考:**T2