# tensorlow . js TF。图模型类〔t1〕

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-graph model-class/

**简介:** Tensorflow.js 是 Google 开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。Tensorflow.js tf。GraphModel 类用于从 SavedModel 构建一个非循环图，并使其推理执行。tf。GraphModel 由 tf.loadGraphModel()方法创建。

**语法:**

```
tf.loadGraphModel.Method(args);
```

**参数:**

*   **Parameters:** Different methods accept different parameters.

**返回:**不同的方法返回不同的数据值等。

下面我们将看到 tf 的一些例子。GraphModel 类:

**示例 1:** 在本例中，我们将看到 executeAsync()方法，该方法用于实现有利于模型的隐含。它以张量为参数，以字符串形式输入输出节点名。它返回张量的承诺。

## Javascript

```
import * as tf from "@tensorflow/tfjs"

async function run(){

// Tensor input elements 
 const gfg_Url =
 'https://storage.googleapis.com/tfjs-models/savedmodel/mobilenet_v2_1.0_224/model.json'; 

// Calling loadGraphModel() function  
 const gfg_Model = await tf.loadGraphModel(gfg_Url); 

// Inputs for the model 
 const gfg_shape = [1, 224, 224, 3];
 const gfg_Input = tf.zeros(gfg_shape);

// Calling executeAsync()  
 const gfg_result = await gfg_Model.executeAsync(gfg_Input); 
 gfg_result.print();

}
await run();
```

**输出:**

```
Tensor
     [[-0.1800359, -0.4059841, 0.8190171, ..., -0.895331,
      -1.084169, 1.2912908],]
```

**示例 2:** 在本例中，我们将看到 dispose()方法，该方法用于处理张量。它不需要任何参数。它返回空。

## Javascript

```
import * as tf from "@tensorflow/tfjs"

async function run(){

// Defining tensor input elements 
 const gfg_Url =
 'https://storage.googleapis.com/tfjs-models/savedmodel/mobilenet_v2_1.0_224/model.json'; 

// Calling the loadGraphModel() funcition  
 const gfg_Model = await tf.loadGraphModel(gfg_Url); 

// Input for our function 
 const gfg_shape = [1, 224, 224, 3];
 const gfg_Input = tf.zeros(gfg_shape);

// Disposing our Tensor 
 const gfg_result = await gfg_Model.executeAsync(gfg_Input);
 gfg_result.dispose();
 console.log(gfg_result) ;

}

await run();
```

**输出:**

```
Tensor is disposed.
```

**参考:**T2】https://js.tensorflow.org/api/latest/#class:GraphModel