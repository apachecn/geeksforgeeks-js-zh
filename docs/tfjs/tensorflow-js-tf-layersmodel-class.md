# tensorlow . js TF。分层模型类〔t1〕

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-layer model-class/

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。张量流。js tf。LayerModel 类用于模型的训练、接口和评估。它有许多训练、评估、预测和保存方法。

**语法:**

```
tf.LayerModel.method(args);
```

**参数:**

*   **args:** Different methods differ in parameters.

**返回:**不同的方法返回不同的值 tf.tensor 对象等。

下面我们将看到 tf 方法的实现。LayerModel 类。

**示例 1:** 在本例中，将看到 trainOnBatch()方法，该方法用于对单批数据应用优化器更新。它取两个张量，第一个作为输入值张量，第二个作为目标张量。它返回一个数字承诺。

## Javascript

```
import * as tf from "@tensorflow/tfjs"

async function run() {

// Training Model 
  const gfg = tf.sequential();

// Adding layer to model  
  const layer = tf.layers.dense({units:3, 
               inputShape : [5]});
   gfg.add(layer);

// Compiling our model 
  const config = {optimizer:'sgd', 
              loss:'meanSquaredError'};
  gfg.compile(config);

// Test tensor and target tensor 
  const layerOne = tf.ones([3,5]);
  const layerTwo = tf.ones([3,3]);

// Apply trainOneBatch to out test data 
  const result =
    await gfg.trainOnBatch(layerOne, layerTwo);

// Printing out result 
  console.log(result);
}

// Function call
await run();
```

**输出:**

```
3.683875560760498
```

**示例 2:** 在本例中，我们将看到 getLayer()方法，该方法借助其索引名称来获取图层。它以图层索引的图层名称作为参数。它返回 TF . layers . layer .

## Javascript

```
import * as tf from "@tensorflow/tfjs"
// Defining model 
 const gfg_Model = tf.sequential(); 

// Adding layers 
 const config = {units: 4, inputShape: [1] };
 const layer = tf.layers.dense( config);;
 gfg_Model.add( layer);

 const config2 = {units: 2, inputShape: [3] , activation: 'sigmoid'};
 const layer2 = tf.layers.dense( config2 );;
 gfg_Model.add(layer2); 

// Calling getLayer() method  
 const layer_1 = gfg_Model.getLayer('denselayer', 1); 

// Printing layer cofig 
 console.log(layer_1.getConfig());
```

**输出:**

```
{
  "units": 2,
  "activation": "sigmoid",
  "useBias": true,
  "kernelInitializer": {
    "className": "VarianceScaling",
    "config": {
      "scale": 1,
      "mode": "fanAvg",
      "distribution": "normal",
      "seed": null
    }
  },
  "biasInitializer": {
    "className": "Zeros",
    "config": {}
  },
  "kernelRegularizer": null,
  "biasRegularizer": null,
  "activityRegularizer": null,
  "kernelConstraint": null,
  "biasConstraint": null,
  "name": "dense_Dense53",
  "trainable": true,
  "batchInputShape": [
    null,
    3
  ],
  "dtype": "float32"
}
```

**参考:**T2】https://js.tensorflow.org/api/latest/#class:LayersModel