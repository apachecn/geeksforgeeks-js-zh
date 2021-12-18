# tensorlow . js TF . browser . topixes()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-browser-topi xels-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-browser-topixels-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**tf.browser.toPixels()** 函数用于在浏览器中将张量转换为图像。

**语法:**

```
tf.browser.toPixels(img, Canvas);
```

**参数:**

*   **img** **(tf。张量 2D|tf。张量 3D|TypedArray|Array):** 形状为[高度，宽度]的秩-2 张量，或形状为[高度，宽度，numChannels]的秩-3 张量。
*   **画布【可选】** **(HTMLCanvasElement):** 要绘制到的画布。

**返回值:**它返回一个承诺，当渲染完成时解决。

**示例 1:** 在本例中，我们创建了一个张量，并用该张量调用 tf.browser.toPixels()函数。

## Javascript

```
import * as tf from "@tensorflow/tfjs"
const tensorA = tf.randomUniform([400, 400, 3]);

tf.browser.toPixels(tensorA).then(() => {
    console.log("tf.browser.toPixels() called");
});
```

**输出:**

```
tf.browser.toPixels() called
```

**示例 2:** 在这个示例中，我们正在创建一个张量并抓取画布引用，并使用张量和画布引用调用 tf.browser.toPixels()函数。

## Javascript

```
const tensorA = tf.randomUniform([400, 400, 3]);

const canvasA = document.getElementById("CanvasHTML");

tf.browser.toPixels(tensorA, canvasA).then(() => {
  tensorA.dispose();
  console.log(
    "Make sure we cleaned up",
    tf.memory().numTensors
  );
});
```

**输出:**

```
Make sure we cleaned up 2
```

**参考:**T2】https://js.tensorflow.org/api/latest/#browser.toPixels