# tensorflow . js TF . enabledebugmode()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-enabledebugmode-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-enabledebugmode-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。enableDebugMode()函数**用于启用调试模式，该模式将记录关于每个执行的内核的数据，即内核实现的跳动时间，包括结果张量的等级、大小以及形状。

**注意:**

*   Debugging mode will greatly slow down the speed of our software, because it will download the final results of every action in the CPU, which cannot be used in production.
*   Debugging mode will not affect the time series data of kernel performance, because the download time here is not evaluated in the kernel performance time.

**语法:**

```
tf.enableDebugMode() 
```

**参数:**此方法不保存任何参数。

**返回值:**返回 void。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling enableDebugMode() method
await tf.enableDebugMode();

// Setting prod mode of the
// environment
tf.env().set('PROD', false);

// Printing output
console.log(tf.env().flags);
```

**输出:**

```
{
  "IS_BROWSER": true,
  "IS_NODE": false,
  "DEBUG": true,
  "CPU_HANDOFF_SIZE_THRESHOLD": 128,
  "PROD": false
}
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling enableDebugMode() method
await tf.enableDebugMode();

// Setting debug mode of the environment
tf.env().set("DEBUG", !0)

// Setting textures of the environment
tf.env().set('WEBGL_FORCE_F16_TEXTURES', true);

// Calling ready() method
await tf.ready();

// Printing output
console.log(tf.env().features);
```

**输出:**

```
{
  "IS_BROWSER": true,
  "IS_NODE": false,
  "DEBUG": true,
  "CPU_HANDOFF_SIZE_THRESHOLD": 128,
  "PROD": true,
  "WEBGL_FORCE_F16_TEXTURES": true,
  "WEBGL_VERSION": 2,
  "HAS_WEBGL": true
}
```

**参考:**T2】https://js.tensorflow.org/api/latest/#enableDebugMode