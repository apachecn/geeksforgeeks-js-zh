# tensorlow . js TF . layers . conv 1d()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-layers-conv 1d-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-layers-conv1d-function/)

Tensorflow.js 是 Google 开发的一个 javascript 库，用于在浏览器或 Node.js 中运行和训练机器学习模型，Tensorflow.js tf.layers.conv1d()函数用于创建卷积层。它用于对输入数据进行一维卷积。卷积层用于制造滤波器，该滤波器用于过滤期望输出中的输入数据。

**语法:**

```
tf.layers.conv1d(args);
```

**参数:**该函数接受以下参数:

*   **Parameters:** This is the object type with the following values:
    *   **Filter:** is a number that defines the dimension of the output tensor. It is the number of filters in convolution.
    *   **Kernel size:** It defines the convolution window of convolution layer, which means that a subset of input data takes effect immediately.
    *   **Step size:** The moving unit of input data is defined by convolution layer of each dimension.
    *   **padding:** It defines the padding of convolution layer, which means the amount of data added to input data during processing. Its values can be "valid", "same" and "causal".
    *   **Data Format:** Defines the data format of input data as' channel first' or' channel last'.
    *   **Expansion rate:** Used to expand the convolution of each dimension. It is used to define the space between values in the kernel.
    *   **Activation:** defines the activation function used by input data.
    *   **Use deviation:** is used to decide whether to use the deviation vector.
    *   [T0】 kernel initializer: 【T1] It is the initial weight of kernel in convolution layer. It defines the method of setting the initial random weight of convolution layer.
    *   [T0】 biasinializer: 【T1] is the initial weight of the bias vector of the convolution layer.
    *   **Kernel constraint:** is a constraint on the convolution layer kernel weight, which is used to improve efficiency.
    *   **Bias constraint:** is a constraint to improve the efficiency of convolution layer bias vector.
    *   **Kernel regularizer:** is a regularizer function applied to the kernel weight matrix to regularize it.
    *   **Offset Regularizer:** It is a regularization function applied to the offset vector to regularize it.
    *   [T0】 activity regulator: 【T1] is a function applied to activation for regularization purposes.
    *   **Input shape:** Declares that this layer accepts the input layer of this shape. It is only used for the input layer.
    *   [T0】 batchInputShape: 【T1] Defines the batch size of the input layer. It is used for the input layer.
    *   **Batch size:** It is a supplement to batchInputShape in the process of making the input layer.
    *   **Data type:** The data type "float32" that defines this layer is the default value of the layer.
    *   **Trainable:** Used to make the layer function trainable or not.
    *   **Weight:** is the initial weight value of this layer.
    *   **Input Type:** is used to determine the data type of the input layer.

**返回:** Conv1D

**示例 1:** 在本例中，我们将创建顺序模型，并使用滤镜、内核大小、输入形状和激活向其添加 1d 卷积层。最后，我们编译了我们的分层模型，并看到它的总结。

## Javascript

```
import * as tf from "@tensorflow/tfjs"

  // Creating model
  const geek_Model  =  tf.sequential();

  // Adding inputLayer layer
  const geek_config = {inputShape: [7,4]};
  const geek_layer1 = tf.layers.inputLayer(geek_config);
  geek_Model.add(geek_layer1);

  // Adding convolution layer
  const geek_config2 = {
    filters:10,kernelSize:7                        
   ,inputShape:[28,1],
    activation: 'relu'};
  const geek_layer2 = tf.layers.conv1d(geek_config2);
   //console.log(y.shape);
   geek_Model.add(geek_layer2);

  // Adding dense layer
  const geek_config3 = {
    units:7,
    activation: 'softmax'
  };
  const geek_layer3 = tf.layers.dense(geek_config3);
  geek_Model.add(geek_layer3)

  // Compiling our model
  const geek_config4 = {
    optimizer: 'sgd',
    loss: 'meanSquaredError'
  };
  geek_Model.compile(geek_config4);

  // Printing our summary
  geek_Model.summary()
```

**输出:**

```
_________________________________________________________________
Layer (type)                 Output shape              Param #   
=================================================================
input1 (InputLayer)          [null,7,4]                0         
_________________________________________________________________
conv1d_Conv1D1 (Conv1D)      [null,1,10]               290       
_________________________________________________________________
dense_Dense1 (Dense)         [null,1,7]                77        
=================================================================
Total params: 367
Trainable params: 367
Non-trainable params: 0
_________________________________________________________________
```

**示例 2:** 在本例中，我们将看到卷积层如何根据配置过滤输入数据。这里我们用输入形状、过滤器、内核大小、激活来制作卷积层，并用它来编译模型。随着卷积层过滤，我们使用预测函数的输入数据。

## Javascript

```
import * as tf from "@tensorflow/tfjs"

// Input Layer for model
const geek_config = {shape:[3,4]};
const geek_InputL = tf.input(geek_config);
console.log(`Input layer shape : ${geek_InputL.shape}`);

// Convolution For the model 
const geek_config2 = {
  filters:2,kernelSize:2                        
 ,inputShape:[3,4],
  activation: 'sigmoid'};
const geek_convLayer = tf.layers.conv1d(geek_config2).apply(geek_InputL);
console.log(`Convolution layer shape : ${geek_convLayer.shape}`);

// Adding layer to the model
const geek_config3 = {inputs:geek_InputL, outputs:geek_convLayer};
const model = tf.model(geek_config3);
// Compiling the model
const geek_config4 = {optimizer:'sgd',loss:'meanSquaredError'};
model.compile(geek_config4);

// Predicting the value for the input
const geek_Test = tf.randomUniform([3,3,4]);
model.predict(geek_Test).print();
```

**输出:**

```
Input layer shape : ,3,4
Convolution layer shape : ,2,2
Tensor
    [[[0.5468831, 0.4990641],
      [0.3059803, 0.4743758]],

     [[0.4450175, 0.4848864],
      [0.3678558, 0.4276305]],

     [[0.4802476, 0.5687023],
      [0.4083693, 0.4854257]]]
```

**参考资料:**[https://js . tensorlow . org/API/3 . 6 . 0/# layers . conv 1d](https://js.tensorflow.org/api/3.6.0/#layers.conv1d)