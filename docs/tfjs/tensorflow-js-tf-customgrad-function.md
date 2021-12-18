# tensorlow . js TF . custom grad()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-custom grad-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-customgrad-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.customGrad()** 函数用于返回指定自定义函数“f”的渐变。这里自定义函数给出{value: Tensor，gradFunc: (dy，saved) → Tensor[]}，其中 gradFunc 给出输入函数 f 相对于其输入的自定义梯度。

**语法:**

```
tf.customGrad(f)
```

**参数:**该函数接受如下所示的参数:

*   **f:** 是指定的自定义功能。

**返回值:**该函数返回指定自定义函数“f”的梯度

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a custom function f
const f = (a, save) => {

   // Saving a for its availablity later for the gradient
   save([a]);

   // Overriding gradient of a^2
   return {
     value: a.square(),

     // Here "saved.a" pointing to "a" which
     // have been saved above
     gradFunc: (dy, saved) => [dy.mul(saved[0].abs())]
   };
}

// Calling the .customGrad() function 
// over the above specified custom function f
const customOp = tf.customGrad(f);

// Initializing a 1D Tensor of some values
const a = tf.tensor1d([0, -1, 1, 2]);

// Getting the gradient of above function
// f for the above specified Tensor values
const da = tf.grad(a => customOp(a));

// Printing the custom function "f" for the
// above specified Tensor "a"
console.log(`f(a):`);
customOp(a).print();

// Printing the gradient of the function "f" for the
// above specified Tensor "a"
console.log(`f'(a):`);
da(a).print();
```

**输出:**

```
f(a):
Tensor
   [0, 1, 1, 4]
f'(a):
Tensor
   [0, 1, 1, 2]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling the .customGrad() function 
// with the custom function "f" as 
// it's parameter
const customOp = tf.customGrad(

// Initializing a custom function f
(a, save) => {

   // Saving a for its availablity later for the gradient
   save([a]);

   // Overriding gradient of a^3
   return {
     value: a.pow(tf.scalar(3, 'int32')),

     // Here "saved.a" pointing to "a" which
     // have been saved above
     gradFunc: (dy, saved) => [dy.mul(saved[0].abs())]
   };
}
);

// Initializing a 1D Tensor of some values
const a = tf.tensor1d([0, -1, 2, -2, 0.3]);

// Getting the gradient of above function
// f for the above specified Tensor values
const da = tf.grad(a => customOp(a));

// Printing the custom function "f" for the
// above specified Tensor "a"
console.log(`f(a):`);
customOp(a).print();

// Printing the gradient of the function "f" for the
// above specified Tensor "a"
console.log(`f'(a):`);
da(a).print();
```

**输出:**

```
f(a):
Tensor
   [0, -1, 8, -8, 0.027]
f'(a):
Tensor
   [0, 1, 2, 2, 0.3]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#customGrad