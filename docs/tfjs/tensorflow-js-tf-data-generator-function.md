# tensorflow . js TF . data . generator()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-generator-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-generator-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf.data.generator()** 函数用于使用生成每个元素的 JavaScript 生成器创建数据集。

**语法:**

```
tf.data.generator(generator)
```

**参数:**

*   **生成器:**是一个 JavaScript 生成器函数，返回一个 JavaScript 迭代器。

**返回值:**返回 tf.data.Dataset。

**示例 1:** 这个示例说明了如何从迭代器工厂创建数据集。

## Javascript

```
// Importing the tensorflow library
import * as tf from "@tensorflow/tfjs"

// Invoking .generator() function
let geek = tf.data.generator(function () {

    // Initializing variables used i.e.  
    // elements, index, result.
    let numbers = 4;
    let indices = 1;
    let outcome;

    // Creating and returning.next() function
    // in the format {value: TensorContainer,
    // done:boolean}.
    let repeator = {
        next: function () {
            if (indices <= numbers) {
                outcome =
                {
                    value: indices,
                    done: false
                };
                indices++;
                return outcome;
            }
            else {
                outcome =
                {
                    value: indices,
                    done: true
                };
                return outcome;
            }
        }
    };
    return repeator;
});

// Printing the result of returned promise
await geek.forEachAsync(function (geeks) {
    console.log(geeks);
});
```

**输出:**

```
1
2
3
4
```

**示例 2:** 此示例说明如何从生成器创建数据集。

## Javascript

```
// Importing the tensorflow library
import * as tf from "@tensorflow/tfjs"

// Creating dataset from .generator() function 
let geek = tf.data.generator(function* () {

    // Initializing variables used i.e.  
    // data, and a.
    let data = 3;
    let a;
    for (i = 0; i <= data; ++i) {
        a = i;
        yield a;
    }
});

// Printing the result of returned promise
await geek.forEachAsync(function (geeks) {
    console.log(geeks);
});
```

**输出:**

```
0
1
2
3
```

**参考:**T2】https://js.tensorflow.org/api/3.6.0/#data.generator