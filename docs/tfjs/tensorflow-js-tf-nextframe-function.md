# tensorlow . js TF . nextframe()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-nextframe-function/

**简介:** Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型以及深度学习神经网络。

**。nextFrame()函数**用于返回一个承诺，该承诺决定了*请求动画帧*终止的时间。

**注:**

*   In this method, Node.js applies *to set* to replace *to request the animation frame* .
*   In addition, this is a basic sugar adding method, and users can do the following.

**语法:**

```
tf.nextFrame()
```

**参数:**此方法不保存任何参数。

**返回值:**返回无效承诺。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using for loop
for(let i = 0; i < 5; i++){

// Calling nextFrame() method
await tf.nextFrame();

// Printing output
console.log('*****');
}
```

**输出:**这里由于 *nextFrame* 法星被一一打印出来。

```
*****
*****
*****
*****
*****
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using for loop
for(let i = 0; i < 3; i++){

// Calling randomNormal() method
const x = tf.randomNormal([2, 3]);

// Calling nextFrame() method
await tf.nextFrame();

// Printing output
console.log(x);
}
```

**输出:**在这里，如果你不止一次地运行程序，那么当张量被处理掉时，就会出现一个错误。

```
Tensor
    [[-1.2814652, 0.0379729, 1.4826748],
     [1.5050254 , 0.0769796, 0.5443317]]
Tensor
    [[-1.9229894, 0.2478886 , 0.6501164],
     [0.3088476 , -1.0728339, 0.8636787]]
Tensor
    [[-0.2324371, -1.2162384, 0.3193687],
     [0.0266885 , 1.3987972 , 0.4429231]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#nextFrame