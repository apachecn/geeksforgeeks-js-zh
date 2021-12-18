# Tensorflow.js tf.tidy()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-tidy-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-tidy-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。tidy()函数**用于执行给定的函数，即 *fn* ，一旦终止，它将清除由所述函数 *fn* 分配的所有等距张量，不包括由 *fn* 返回的等距张量。在此， *fn* 不应产生*承诺*。然而，返回的输出可能是一个复杂的对象。

**注意:**

*   This method is beneficial to prevent memory leakage. Generally, the wrap calls the process in the tf.tidy () function to automatically clean up the memory.
*   However, the variable is not cleared in the *tidy ()* function. If you want to dispose of variables, you can use *TF. DisposeVariables ()* or call the *Dispose ()* method on variables immediately.

**语法:**

```
tf.tidy(nameOrFn, fn?)
```

**参数:**

*   **Namer:** The specified name of the stopper or the function to be performed. If a name is given, then the second parameter must be a function. And if the debug mode is turned on, the scheduling and the memory utilization of the function will be performed with the given designation and displayed on the console. It can be a string or a function type.
*   **fn:** The specified function to be executed. It is optional and belongs to function type.

**返回值:**返回 void、number、string、TypedArray、tf。张量。Tensor[]，或{[key: string]:tf。张量、数字或字符串}。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling tidy() method
const res = tf.tidy(() => {

   // Calling scalar() method
   const x = tf.scalar(3);

   // Calling sqrt() function
   const y = tf.sqrt(5);

   // Calling square() method
   const z = y.square();

  // Calling sub() method 
  return z.sub(x);
});

// Printing output
res.print();
```

**输出:**

```
Tensor
    2
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling tidy() method
const res = tf.tidy(() => {

   // Calling sin() method
   const op = tf.sin(45);

   // Printing number of tensors inside tidy
   // Using memory() method
   console.log('number of tensors inside tidy: '
      + tf.memory().numTensors);

  // Calling sqrt() method 
  return op.sqrt();
});

   // Printing number of tensors outside tidy
   // Using memory() method
   console.log('number of tensors outside tidy: '
      + tf.memory().numTensors);

// Printing output
res.print();
```

**输出:**

```
number of tensors inside tidy: 1
number of tensors outside tidy: 1
Tensor
    0.9224448204040527
```

**参考:**T2】https://js.tensorflow.org/api/latest/#tidy