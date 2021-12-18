# Tensorflow.js tf。LayersModel 类。fitDataset()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers model-class-fitdataset-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-layersmodel-class-fitdataset-method/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。Tensorflow.js tf。LayersModel 类。fitDataset()方法用于通过使用数据集对象来训练图层模型。

**语法:**

```
LayerModel.fitDataset(dataset, args);
```

**参数:**该方法接受以下参数:

*   **Dataset:** It is the input value in the form of dataset, and we use it to train our layer model.
*   **args:** is an object with the following values:
    *   [T0】 batchespercEpoch: 【T1] is the number of batches in each epoch. It depends on the batch size. As the batch size increases, its size will also decrease.
    *   **Era:** is the total number of iterations in the training data set during the training model. It should be an integer value.
    *   **initialepoch:** used to define the epoch value for starting training.
    *   **Validity data:** is used to give the estimated value of the final model when choosing between the final models.
    *   **Details:** It helps to show the progress of each era. If the value is 0–it means that no message was printed during the fit () call. If the value is 1–this means that in Node.js, it will print a progress bar. In the browser, it does not display any actions. A value of 1 is the default value. 2–The value 2 has not been implemented.
    *   **classweight:** Used to weight the loss function. It may be useful to tell the model to pay more attention to the samples from the classes that are insufficient.
    *   **Callback:** It defines the callback list to be called during training. A variable can have one or more callbacks onTrainBegin (), onTrainEnd (), onEpochBegin (), onEpochEnd (), onBatchBegin (), onBatchEnd (), onYield ().
    *   [T0】 validationBatchSize: 【T1 is a number that defines the batch size. It is used to verify the batch size. This means that we can't put all data sets that exceed this value at once. Its default value is 32.
    *   **Verification batch:** Used to verify the sample batch. It is used to draw validation data for validation at the end of each period.
    *   [T0】 yield they: 【T1] It defines the configuration of the frequency of giving the main thread to other tasks. It can be automatic, which means that yielding occurs at a certain frame rate. Batch, if the value is this, it will generate each batch. Era, if the value is this, it generates each era. Any number, if the value is any number, it generates a number every millisecond. Never, if the value is this, it will never yield.

**回报:**承诺<历史>

**示例 1:** 在本例中，我们将使用 CSV 数据集训练我们的图层模型。

## Javascript

```
import * as tf from "@tensorflow/tfjs"

// Path for the CSV file 
const gfg_CsvFile =
'https://storage.googleapis.com/tfjs-examples/multivariate-linear-regression/data/boston-housing-train.csv';

async function run() {

    // Creating model
    const gfg_LayerModel = tf.sequential();

    // Adding layer to model
    const config = { units: 1, inputShape: [12] }
    const gfg_layer = tf.layers.dense(config);
    gfg_LayerModel.add(gfg_layer);

    // Compiling the model
    const opt = tf.train.sgd(0.00000001)
    gfg_LayerModel.compile({ optimizer: opt, 
            loss: 'meanSquaredError' });

    // Here we want to predict column tax
    const config2 = { columnConfigs: {
             rad: { isLabel: true } } };

    const csvDataset = tf.data.csv(gfg_CsvFile, config2);

    // Creating dataset for training
    const flattenedDataset =
        csvDataset.map(({ xs, ys }) => {
            return { xs: Object.values(xs), 
                    ys: Object.values(ys) };
        }).batch(6);

    // Training the model
    const Tm = await gfg_LayerModel.fitDataset(
            flattenedDataset, { epochs: 10 });

    for (let i = 0; i < 6; i++) {
        console.log(Tm.history.loss[i])
    }
}
run();
```

**输出:**

```
41480.109375
28887.93359375
20162.228515625
14115.478515625
9924.9404296875
7020.56005859375
```

**示例 2:** 在本例中，我们将使用阵列的数据集训练我们的图层模型。

## Javascript

```
import * as tf from "@tensorflow/tfjs"

async function run() {

    // Creating Layer model
    const gfg_LayerModel = tf.sequential();

    // Adding layer to model
    const config = { units: 4, inputShape: [4] }
    const gfg_layer = tf.layers.dense(config);
    gfg_LayerModel.add(gfg_layer);

    // Compiling the model
    const config2 = { optimizer: 'sgd', loss: 'meanSquaredError' }
    gfg_LayerModel.compile(config2);

    // Creating Datasets for training
    const array1 = [
        [1, 2, 3, 4],
        [1, 4, 6, 8],
        [1, 3, 4, 7],
        [3, 4, 7, 8]
    ];
    const array2 = [1, 1, 1, 1];
    const arrData1 = tf.data.array(array1);
    const arrData2 = tf.data.array(array2);

    const config3 = { xs: arrData1, ys: arrData2 }
    const arrayDataset = tf.data.zip(config3)
    const ArrayDataset = arrayDataset.batch(4);

    // Training the model
    const Tm = await gfg_LayerModel.fitDataset(
            ArrayDataset, { epochs: 4 });

    // Printing the loss after training
    console.log("Loss After Training Layer Model"
        + Tm.history.loss[0]);
}
run();
```

**输出:**

```
Loss After Training Layer Model 4.386415958404541
```

**参考:**[https://js.tensorflow.org/api/latest/#tf.LayersModel.fitDataset](https://js.tensorflow.org/api/latest/#tf.LayersModel.fitDataset)