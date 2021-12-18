# tensorflow . js TF . layers . inputlayer()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-input layer-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-inputlayer-function/)

[Tensorflow.js](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**tf.layers.inputLayer()函数**是指向 *tf 的入口点。layer model*。它是为了支持 *tf 而自发产生的。顺序模型*通过定义*输入形状*或 *batchInputShape* 来支持第一层。不能特别定义。此外，周期性地是有益的，例如，当从其他顺序模型层的子集创建顺序模型时。

**语法:**

```
tf.layers.inputLayer(args)
```

**参数:**

*   **args:** 以上方法可以成立的陈述论点。它属于 object 类型，它包含的参数如下所示。
    1.  **输入形状:**不包括批次轴的所述输入形状。它的类型可以是(null | number)[]。
    2.  **批次大小:**是指定的可选输入批次大小。它可以是整数或 null 类型。
    3.  **批处理输入形状:**是所述的批处理输入形状，包括批处理轴。它的类型可以是(null | number)[]。
    4.  **数据类型:**所述输入的数据类型。它可以是类型 *float32、int32、bool、complex64* 或 *string* 。
    5.  **稀疏:**表示创建的占位符是否是稀疏的。它是布尔型的。
    6.  **名称:**正在使用的图层的指定名称。它属于字符串类型。

**返回值:**返回输入层。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining a model
const model = tf.sequential();

// Calling layers.inputLayer() using add() method
model.add(tf.layers.inputLayer({inputShape: [4]}));

// Printing output
model.predict(tf.ones([1, 4])).print();
```

**输出:**

```
Tensor
     [[1, 1, 1, 1],]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining a model
const model = tf.sequential();

// Calling layers.inputLayer() method using add() method
model.add(tf.layers.inputLayer({batchInputShape: [4], 
      dtype: 'int32', sparse: false, name: 'mlayer'}));

// Printing output
model.summary();
```

**输出:**

```
_________________________________________________________________
Layer (type)                 Output shape              Param #   
=================================================================
mlayer (InputLayer)          [4]                       0         
=================================================================
Total params: 0
Trainable params: 0
Non-trainable params: 0
_________________________________________________________________
```

**参考:**T2】https://js.tensorflow.org/api/latest/#layers.inputLayer