# Tensorflow.js tf。LayersModel 类。评估数据集()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers model-class-evaluatedataset-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layersmodel-class-evaluatedataset-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。evaluateDataset()函数**用于通过指定的数据集对象来评估指定的模型。

**注意:**此方法与 evaluate()不同，因为它是异步的。

**语法:**

```
evaluateDataset(dataset, args?)
```

**参数:**

*   **Data set:** The data set object. In order to generate a dataset iterator object, you need to wait for its iterator () method, and then wait for its next () method to generate a data batch for calculation. In addition, the return value of the next () call must contain a boolean done field and a value field. The value field may be an array of two TFS. Tensor or an array of two nested tf. Tensor construction. The first case is the model with only one input and one output, that is, the sequential model. The latter case benefits the model and several inputs and/or several outputs. Of the two elements in the array, the first is the input feature and the second is the output target. Its type is tf.data.dataset. 。
*   [T0】 args: 【T1] The configuration object described in **supports the evaluation based on data set. It is optional and belongs to the object type. The following parameters are included:**
    1.  **Batch:** The specified number of batches to be dragged from the given dataset object before terminating the evaluation. It's of numerical type.
    2.  **Detail:** State the detail mode. Type *model detail* .

**返回值:**返回 tf 的承诺。标量或 tf。标量[]。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining an array x
const Array_x = [
   [1, 1, 1, 1, 1, 1, 1, 1],
   [1, 1, 1, 1, 1, 1, 1, 1],
   [1, 1, 1, 1, 1, 1, 1, 1],
   [1, 1, 1, 1, 1, 1, 1, 1],
];

// Defining an array y
const Array_y = [1, 1, 1, 1];

// Defining dataset of x
const Dataset_x = tf.data.array(Array_x);

// Defining dataset of y
const Dataset_y = tf.data.array(Array_y);

// Defining dataset of xy using zip method
const Dataset_xy = tf.data.zip({xs: Dataset_x, ys: Dataset_y})
     .batch(5)
     .shuffle(3);

// Defining model
const mymodel = tf.sequential({
   layers: [tf.layers.dense({units: 1, inputShape: [8]})]
});

// Compiling model
mymodel.compile({optimizer: 'sgd', loss: 'meanSquaredError'});

// Calling evaluateDataset() method
const res = await mymodel.evaluateDataset(Dataset_xy, 
tf.ones([7, 10]), tf.ones([7, 1]), {
   batchSize: 5,
});

// Printing output
res.print();
```

**输出:**

```
Tensor
    0.9196577668190002
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining dataset of xy using zip method
const Dataset_xy = tf.data.zip({
    xs: tf.data.array([[1, 0, 1, 2, 1]]), 
    ys: tf.data.array([1, 2, 1, 3])})
    .batch(8);

// Defining model
const mymodel = tf.sequential({
   layers: [tf.layers.dense(
      {units: 1, inputShape: [5], activation: 'sigmoid'})
   ]
});

// Compiling model
mymodel.compile({optimizer: 'sgd', loss: 'meanSquaredError'});

// Calling evaluateDataset() method
const res = await mymodel.evaluateDataset(
    Dataset_xy, tf.truncatedNormal([7, 10]), 
        tf.randomNormal([7, 1]), 
        {batchSize: 2, steps: 1}
    );

// Printing output
console.log(JSON.stringify(res));
```

**输出:**

```
{"kept":false,"isDisposedInternal":false,"shape":[],"dtype":"float32",
"size":1,"strides":[],"dataId":{"id":6923},"id":4594,
"rankType":"0","scopeId":4223}
```

**参考:**[https://js.tensorflow.org/api/latest/#tf.图层模型评估数据集](https://js.tensorflow.org/api/latest/#tf.LayersModel.evaluateDataset)