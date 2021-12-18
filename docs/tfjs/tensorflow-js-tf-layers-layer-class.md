# tensorflow . js TF . layers . layer 类

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-layer-class/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-layer-class/)

**简介:** Tensorflow.js 是 Google 开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。 **tf.layers.Layer 类**用于扩展序列化。可序列化的类。此外，一个层是一组进程以及权重的集合，这些权重可以被收集来构建一个 tf.LayersModel。

这个 **tf.layers.Layer 类**包含十个内置方法，如下图所示:

*   层类[敷](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-apply-method/)()法
*   层类计数参数()方法
*   层类[构建](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-build-method/)()方法
*   层类获取权重()方法
*   Tf.layers.Layer class. [Method for setting weight](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-setweights-method/) ()
*   Tf.layers.Layer class. [Method of adding weight](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-addweight-method/) ()
*   层类[添加损耗](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-addloss-method/)()方法
*   层类[计算输出形状](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-computeoutputshape-method/)()方法
*   层类 [getConfig](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-getconfig-method/) ()方法
*   层类[处置](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-dispose-method/)()法

**1。tf.layers.Layer 类。apply()方法:**当我们用 tf 调用它时，它用于执行 Layers 计算并返回 Tensor。张量。如果我们叫它 tf。然后，它将为将来的执行准备层。

**例:**

## Javascript

```
import * as tf from "@tensorflow/tfjs"

const denseLayer = tf.layers.dense({
units: 1,
kernelInitializer: 'ones',
useBias: false
});

const input = tf.ones([2, 2]);
const output = denseLayer.apply(input);

// Print the output
print(output)
```

**输出:**

```
Tensor [[2], [2]]
```

**2。tf.layers.Layer 类。countParams()方法:**用于求规定权重中 float32、int32 等数字的绝对计数。

**例:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding a layer
model.add(tf.layers.dense({units: 2, inputShape: [11]}));

// Calling setWeights() method
model.layers[0].setWeights(
    [tf.truncatedNormal([11, 2]), tf.zeros([2])]);

// Calling countParams() method and also
// Printing output
console.log(model.layers[0].countParams());
```

**输出:**

```
24
```

**3。tf.layers.Layer 类。build()方法:**用于创建所述层的权重。这种方法应该适用于每一个持有权重的层。此外，当调用 apply()方法来构建权重时，它会被调用。

**例:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding a layer
model.add(tf.layers.dense({units: 1, inputShape: [3]}));

// Defining input
const input = tf.input({shape: [6, 2, 6]});

// Calling build method with its
// parameter
model.layers[0].build([input.Shape]);

// Printing output
console.log(JSON.stringify(input.shape));
model.layers[0].getWeights()[0].print();
```

**输出:**

```
[null,6,2,6]
Tensor
    [[-0.3726568],
     [0.7343086 ],
     [-0.2459907]]
```

**4。tf.layers.Layer 类。getWeights()方法:**用于获取一个张量的权值。

**例:**

## Javascript

```
// Creating a model
const model = tf.sequential();

// Adding layers
model.add(tf.layers.dense({units: 2, inputShape: [5]}));
model.add(tf.layers.dense({units: 3}));

model.compile({loss: 'categoricalCrossentropy', optimizer: 'sgd'});

// Printing the weights of the layers
model.layers[0].getWeights()[0].print()
model.layers[0].getWeights()[1].print()
```

**输出:**

```
Tensor
    [[-0.4756567, 0.2925433 ],
     [0.3505997 , -0.5043278],
     [0.5344347 , 0.2662918 ],
     [-0.1357223, 0.2435055 ],
     [-0.6059403, 0.1990891 ]]
Tensor
    [0, 0]
```

**5。tf.layers.Layer 类。setWeights()方法:**用于根据给定的张量设置所述层的权重。

**例:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding a layer
model.add(tf.layers.dense({units: 2, inputShape: [11]}));

// Calling setWeights() method
model.layers[0].setWeights([tf.truncatedNormal([11, 2]), tf.zeros([2])]);

// Compiling the model
model.compile({loss: 'categoricalCrossentropy', optimizer: 'sgd'});

// Printing output using getWeights() method
model.layers[0].getWeights()[0].print();
```

**输出:**

```
Tensor
    [[-0.5969906, -0.1883931],
     [0.8569255 , -0.49416  ],
     [0.1157023 , 0.1150239 ],
     [-0.4052143, 1.9936075 ],
     [0.3090054 , 0.7212474 ],
     [0.4626641 , -0.7287846],
     [0.4352857 , -0.5195332],
     [0.4626429 , 0.0216295 ],
     [-0.1110666, -0.5997615],
     [-0.5083916, -0.3582681],
     [-0.2847465, 1.184485  ]]
```

**6。** **tf.layers.Layer 类。addWeight()方法:**用于向所述层添加权重变量。

**例:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding a layer
model.add(tf.layers.dense({units: 2, inputShape: [1]}));

// Calling addWeight() method
const res = model.layers[0].addWeight('wt_var',
        [1, 5], 'int32', tf.initializers.ones());

// Printing output
console.log(res);
model.layers[0].getWeights()[0].print();
```

**输出:**

```
{
  "dtype": "int32",
  "shape": [
    1,
    5
  ],
  "id": 1582,
  "originalName": "wt_var",
  "name": "wt_var_2",
  "trainable_": true,
  "constraint": null,
  "val": {
    "kept": false,
    "isDisposedInternal": false,
    "shape": [
      1,
      5
    ],
    "dtype": "int32",
    "size": 5,
    "strides": [
      5
    ],
    "dataId": {
      "id": 2452
    },
    "id": 2747,
    "rankType": "2",
    "trainable": true,
    "name": "wt_var_2"
  }
}
Tensor
     [[0.139703, 0.9717236],]
```

**7。tf.layers.Layer 类。addLoss()方法:**用于将损耗附加到所述层。此外，损耗可能取决于一些输入张量，例如，操作损耗取决于所述层的输入。

**例:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding a layer
model.add(tf.layers.dense({units: 1, inputShape: [3]}));

// Defining input
const input = tf.tensor1d([1, 2, 3, 4]);

// Calling addLoss() method with its
// parameter
const res = model.layers[0].addLoss([tf.abs(input)]);

// Printing output
console.log(JSON.stringify(input));
model.layers[0].getWeights()[0].print();
```

**输出:**

```
{"kept":false,"isDisposedInternal":false,
"shape":[4],"dtype":"float32",
"size":4,"strides":[],"dataId":{"id":82},
"id":124,"rankType":"1","scopeId":61}
Tensor
    [[0.143441  ],
     [-0.58002  ],
     [-0.5836995]]
```

**8。tf.layers.Layer 类。computeOutputShape()方法:**用于枚举所述图层的输出形状。并且假定将创建该层，以便与所提供的输入形状相匹配。

**例:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding a layer
model.add(tf.layers.dense({units: 1, inputShape: [3]}));

// Defining inputShape
const inputShape = [6, 2, 6];

// Calling computeOutputShape() method with its
// parameter
const val = model.layers[0].computeOutputShape(inputShape);

// Printing output
console.log(val);
```

**输出:**

```
6,2,1
```

**9。tf.layers.Layer 类。getConfig()方法:**用于获取一个图层的配置。

**例:**

## Javascript

```
const tf = require("@tensorflow/tfjs")

// Creating a minLayer
const minLayer = tf.layers.minimum();

// Getting the configuration of the layer
const config = minLayer.getConfig();
console.log(config)
```

**输出:**

```
{ name: 'minimum_Minimum1', trainable: true }
```

**10。** **tf.layers.Layer 类。dispose()方法:**用于处理所述层的重量。此外，它通过 1 减少所述层对象的参考计数。

**例:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a model
const model = tf.sequential();

// Adding a layer
model.add(tf.layers.dense({units: 1, inputShape: [3]}));

// Calling dispose method
const val = model.layers[0].dispose();

// Printing output
console.log(val);
```

**输出:**

```
{
  "refCountAfterDispose": 0,
  "numDisposedVariables": 2
}
```

**参考:**T2】https://js.tensorflow.org/api/latest/#class:layers.Layer