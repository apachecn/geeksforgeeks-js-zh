# Tensorflow.js tf。顺序类.预测()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sequential-class-predict-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-sequential-class-predict-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。predict()方法**用于在考虑所述输入实例的情况下产生输出期望。此外，这里的计算是分组进行的。

**语法:**

```
predict(x, args?)
```

**参数:**

*   **x:** 它是陈述的输入数据，像张量，或者 tf 的数组。张量，以防模型有大量输入。它可以是 tf 类型。张量或 tf。张量[]。
*   **参数:**是一个可选参数，类型为 object。
    1.  **批处理大小:**是以整数形式表示的批处理大小，是可选参数。此外，如果未指定，则默认值为 32。
    2.  **详细:**是默认为假的陈述详细模式。它属于布尔类型，是可选的。

**返回值:**返回 tf。张量或 tf。张量[]。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining model
const modl = tf.sequential({
   layers: [tf.layers.dense({units: 2, inputShape: [40]})]
});

// Calling predict() method and
// Printing output
modl.predict(tf.truncatedNormal([7, 40])).print();
```

**输出:**

```
Tensor
    [[0.1556173 , 1.2365075 ],
     [-1.7945877, 2.3424799 ],
     [0.3632407 , -0.1731701],
     [0.195157  , -0.7823027],
     [0.4565429 , 2.512109  ],
     [-1.2392806, 0.1868197 ],
     [0.6895663 , -0.2006246]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling predict() method and
// Printing output
tf.sequential({
   layers: [tf.layers.dense({units: 3, inputShape: [20]})]
}).predict(tf.randomNormal([8, 20])).print();
```

**输出:**

```
Tensor
    [[-1.1149288, 0.8968778 , -0.7492741],
     [1.3654473 , -0.471923 , 1.3632329 ],
     [0.5550661 , 0.6949158 , 1.9761562 ],
     [-0.2109454, -0.3558912, 0.243051  ],
     [-1.2827762, 0.5370077 , 0.1645843 ],
     [0.1542411 , -1.359634 , -0.1656512],
     [-0.4721956, 0.3904444 , 0.7398967 ],
     [-0.2076109, -3.0447464, 1.3338548 ]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#tf.Sequential.predict