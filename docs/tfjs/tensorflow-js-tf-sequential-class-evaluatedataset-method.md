# Tensorflow.js tf。顺序类。评估数据集()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sequential-class-evaluatedataset-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-sequential-class-evaluatedataset-method/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。evaluateDataset()函数**用于通过指定的数据集对象评估指定的序列模型。

**注意:**此方法与 evaluate()不同，因为它是异步的。

**语法:**

```
evaluateDataset(dataset, args?)
```

**参数:**

*   **Data set:** The data set object. In order to generate the dataset iterator object, we need to wait for its iterator () method, and then wait for its *next* () method to generate the data batch for evaluation. In addition, the return value of the next () call must contain a Boolean value <sub>done</sub> field and a <sub>value</sub> field. The value field may be an array of two TFS. Tensor or an array of two nested tf. Tensor construction. The first case is that the model has only one input and one output (such as ... sequential model). The latter case benefits the model and several inputs and/or several outputs. Of the two elements in the array, the first is the input feature and the second is the output target. The type is *TF.data.dataset* .
*   **Parameters:** The configuration object supports data set-based evaluation. It is optional and belongs to the object type. The following parameters are included:
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

// Training Model 
const gfg = tf.sequential();

// Adding layer to model  
const layer = tf.layers.dense({units:1, 
               inputShape : [8]});
   gfg.add(layer);

// Compiling our model 
const config = {optimizer:'sgd', 
              loss:'meanSquaredError'};
  gfg.compile(config);

// Calling evaluateDataset() method
const res = await gfg.evaluateDataset(Dataset_xy, 
tf.ones([7, 10]), tf.ones([7, 1]), {
   batchSize: 5,
});

// Printing output
res.print();
```

**输出:**

```
Tensor
    2.9478049278259277
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining dataset of xy using zip method
const Dataset_xy = tf.data.zip({
    xs: tf.data.array([[1, 0, 1, 2, 1]]), 
    ys: tf.data.array([1, 2, 1, 3])}).batch(8);

// Training Model 
const gfg = tf.sequential();

// Adding layer to model  
const layer = tf.layers.dense({units:1, 
    inputShape : [5], activation: 'sigmoid'});

gfg.add(layer);

// Compiling our model 
const config = {optimizer:'sgd', 
              loss:'meanSquaredError'};

gfg.compile(config);

// Calling evaluateDataset() method
const res = await gfg.evaluateDataset(
    Dataset_xy, tf.truncatedNormal([7, 10]), 
    tf.randomNormal([7, 1]), 
    {batchSize: 2, steps: 1});

// Printing output
console.log(JSON.stringify(res));
```

**输出:**

```
{"kept":false,"isDisposedInternal":false,"shape":[],
"dtype":"float32","size":1,"strides":[],"dataId":{"id":7097},
"id":4731,"rankType":"0","scopeId":4352}
```

**参考:**[https://js.tensorflow.org/api/latest/#tf.顺序评估数据集](https://js.tensorflow.org/api/latest/#tf.Sequential.evaluateDataset)