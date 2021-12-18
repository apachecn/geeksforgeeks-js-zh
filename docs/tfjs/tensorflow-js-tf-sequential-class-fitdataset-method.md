# Tensorflow.js tf。顺序类。fitDataset()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sequential-class-fit dataset-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-sequential-class-fitdataset-method/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。Tensorflow.js tf。顺序类。fitDataset()方法用于使用数据集对象训练模型。

**语法:**

```
model.fitDataset(dataset, args);
```

**参数:**该方法包含以下参数:

*   **Data set:** is a data set with input values. It can be a primitive dataset, an array or an object.
*   **args:** It contains the following values:
    *   **Era:** It is the total number of passes in the training data set during the training model. It is an integer value.
    *   **Batch Period:** Defines the batch quantity of each period. Its value depends on the batch size, and as the batch size increases, its size will also decrease.
    *   **Details:** It helps to show the progress of each era. If the value is 0–it means that no message was printed during the fit () call. If the value is 1–this means that in Node.js, it will print a progress bar. In the browser, it does not display any actions. A value of 1 is the default value. 2–The value 2 has not been implemented.
    *   **Callback:** It defines the callback list to be called during training. A variable can have one or more callbacks onTrainBegin (), onTrainEnd (), onEpochBegin (), onEpochEnd (), onBatchBegin (), onBatchEnd (), onYield ().
    *   **Validity data:** is used to give the estimated value of the final model when choosing between the final models. This can be any of the following: an [xVal, yVal] array, a dataset object containing elements of the form {xs: xVal, ys: yVal}.
    *   [T0】 validationBatchSize: 【T1 is a number that defines the batch size. It is used to verify the batch size. This means that we can't put all data sets that exceed this value at once. Its default value is 32.
    *   **Verification batch:** Used to verify the sample batch. It is used to draw validation data for validation at the end of each period.
    *   **classweight:** Used to weight the loss function. It may be useful to tell the model to pay more attention to the samples from the classes that are insufficient.
    *   **initialepoch:** used to define the epoch value for starting training. This is very useful for resuming the previous training.
    *   [T0】 yield they: 【T1] It defines the configuration of the frequency of giving the main thread to other tasks. It can be automatic, which means that yielding occurs at a certain frame rate. Batch, if the value is this, it will generate each batch. Era, if the value is this, it generates each era. Any number, if the value is any number, it generates a number every millisecond. Never, if the value is this, it will never yield.

**回报:**承诺<历史>

**示例 1:** 在本例中，我们将使用数组数据集训练模型。

## Javascript

```
import * as tf from "@tensorflow/tfjs"

// Creating model
const gfg_Model = tf.sequential() ;

// Adding layer to model
const config = {units: 1, inputShape: [2]}
const gfg_layer = tf.layers.dense(config);
gfg_Model.add(gfg_layer);

// Compiling the model
const config2 = {optimizer: 'sgd', loss: 'meanSquaredError'} 
gfg_Model.compile(config2);

// Creating Datasets for training
const array1 = [[1,2], [1,4], [1,3], [3,4]];
const array2 = [1, 1];
const arrData1 = tf.data.array(array1);
const arrData2 = tf.data.array(array2);

const config3 = {xs:arrData1, ys:arrData2}
const arrayDataset = tf.data.zip(config3)
const ArrayDataset = arrayDataset.batch(3).shuffle(6);

// Training the model
const Tm = await gfg_Model.fitDataset(ArrayDataset, { epochs: 3 });

// Printing the loss after training
console.log("Loss " + " : " + Tm.history.loss[0]);
```

**输出:**

```
Loss : 0.428712397813797
```

**示例 2:** 在本例中，我们将使用由 csv 文件制作的数据集来训练我们的模型。

## Javascript

```
import * as tf from "@tensorflow/tfjs";

// Path for the CSV file
const gfg_CsvFile =
  "https://storage.googleapis.com/tfjs-examples/multivariate-linear-regression/data/boston-housing-train.csv";

// Creating model
const gfg_Model = tf.sequential();

// Adding layer to model
const config = { units: 1, inputShape: [12] };
const gfg_layer = tf.layers.dense(config);
gfg_Model.add(gfg_layer);

// Compiling the model
const opt = tf.train.sgd(0.0001);
gfg_Model.compile({ optimizer: opt, loss: "meanSquaredError" });

// Here we want to predict column tax
const config2 = { columnConfigs: { tax: { isLabel: true } } };
const csvDataset = tf.data.csv(gfg_CsvFile, config2);

// Creating dataset for training
const flattenedDataset = csvDataset
  .map(({ xs, ys }) => {
    return { xs: Object.values(xs), ys: Object.values(ys) };
  })
  .batch(5);

// Training the model
const Tm = await gfg_Model.fitDataset(flattenedDataset, { epochs: 5 });

for (let i = 0; i < 5; i++) {
  console.log(Tm.history.loss[i]);
}
```

**输出:**

```
21489.68359375
8750.29296875
6632.365234375
5908.6171875
5546.45654296875
```

**参考:**[https://js.tensorflow.org/api/latest/#tf.顺序. fitDataset](https://js.tensorflow.org/api/latest/#tf.Sequential.fitDataset)