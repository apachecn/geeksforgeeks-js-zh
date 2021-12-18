# tensorlow . js TF . enableprod mode()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-enable prod mode-function/

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。启用生产模式()功能**用于启用生产模式，以取消支持生产的精确约束。

**语法:**

```
tf.enableProdMode()
```

**参数:**此方法不保存任何参数。

**返回值:**返回 void。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling enableProdMode() method
await tf.enableProdMode();

// Setting debug mode of the
// environment
tf.env().set('DEBUG', false);

// Printing output
console.log(tf.env().flags);
```

**输出:**

```
{
  "IS_BROWSER": true,
  "IS_NODE": false,
  "DEBUG": false,
  "CPU_HANDOFF_SIZE_THRESHOLD": 128,
  "PROD": true,
  "WEBGL_VERSION": 2,
  "HAS_WEBGL": true,
  "WEBGL_CHECK_NUMERICAL_PROBLEMS": false,
  "IS_TEST": false,
  "WEBGL_CPU_FORWARD": true,
  "WEBGL_MAX_TEXTURE_SIZE": 16384,
  "WEBGL_FORCE_F16_TEXTURES": true,
  "WEBGL_RENDER_FLOAT32_CAPABLE": true,
  "WEBGL_RENDER_FLOAT32_ENABLED": true,
  "WEBGL_FLUSH_THRESHOLD": -1,
  "WEBGL_PACK": true,
  "WEBGL_LAZILY_UNPACK": true,
  "WEBGL_DELETE_TEXTURE_THRESHOLD": -1,
  "WEBGL_PACK_BINARY_OPERATIONS": true,
  "WEBGL_USE_SHAPES_UNIFORMS": false,
  "WEBGL_PACK_UNARY_OPERATIONS": true,
  "WEBGL_DOWNLOAD_FLOAT_ENABLED": true,
  "WEBGL_CONV_IM2COL": true,
  "WEBGL_PACK_DEPTHWISECONV": true,
  "WEBGL_MAX_TEXTURES_IN_SHADER": 16,
  "WEBGL_PACK_ARRAY_OPERATIONS": true
}
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling enableProdMode() method
await tf.enableProdMode();

// Setting prod mode of the environment
tf.env().set("PROD", !0)

// Setting textures of the environment
tf.env().set('WEBGL_FORCE_F16_TEXTURES', false);

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
  "DEBUG": false,
  "CPU_HANDOFF_SIZE_THRESHOLD": 128,
  "PROD": true,
  "WEBGL_VERSION": 2,
  "HAS_WEBGL": true,
  "WEBGL_CHECK_NUMERICAL_PROBLEMS": false,
  "IS_TEST": false,
  "WEBGL_CPU_FORWARD": true,
  "WEBGL_MAX_TEXTURE_SIZE": 16384,
  "WEBGL_FORCE_F16_TEXTURES": false,
  "WEBGL_RENDER_FLOAT32_CAPABLE": true,
  "WEBGL_RENDER_FLOAT32_ENABLED": true,
  "WEBGL_FLUSH_THRESHOLD": -1,
  "WEBGL_PACK": true,
  "WEBGL_LAZILY_UNPACK": true,
  "WEBGL_DELETE_TEXTURE_THRESHOLD": -1,
  "WEBGL_PACK_BINARY_OPERATIONS": true,
  "WEBGL_USE_SHAPES_UNIFORMS": false,
  "WEBGL_PACK_UNARY_OPERATIONS": true,
  "WEBGL_DOWNLOAD_FLOAT_ENABLED": true,
  "WEBGL_CONV_IM2COL": true,
  "WEBGL_PACK_DEPTHWISECONV": true,
  "WEBGL_MAX_TEXTURES_IN_SHADER": 16,
  "WEBGL_PACK_ARRAY_OPERATIONS": true
}
```

**参考:**T2】https://js.tensorflow.org/api/latest/#enableProdMode