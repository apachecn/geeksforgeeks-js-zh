# tensorflow . js TF . set 后端()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-set 后端-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-setbackend-function/)

[**tensorflow . js**](https://www.geeksforgeeks.org/introduction-to-tensorflow/)是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**TF .set 后端()**功能用于设置当前后端名称。

**语法:**

```
tf.setBackend( backendName )
```

**参数:**

*   **后端名称:**后端的名称。

**返回值:**返回承诺<布尔>

**示例 1:** 在本例中，我们将后端设置为字符串“cpu”。然后它被设置为字符串“webgl”，后端被移除，返回“null”字符串。

## Javascript

```
// Setting the backend
tf.setBackend("cpu")
console.log(tf.getBackend())

tf.setBackend("webgl")
tf.removeBackend("webgl")
console.log(tf.getBackend())
```

**输出:**

```
cpu
null
```

**示例 2:** 在本例中，我们将后端设置为字符串“cpu”。后端被移除，在控制台中返回“空”。我们将后端设置为“webgl”，将后端作为字符串“webgl”返回。

## Javascript

```
// Setting the backend
tf.setBackend("cpu")
tf.removeBackend('cpu')
console.log(tf.getBackend())

tf.setBackend("webgl")

// Getting the backend using
// getBackend method
console.log(tf.getBackend())
```

**输出:**

```
null
webgl
```

**参考:**[https://js.tensorflow.org/api/latest/#setBackend](https://js.tensorflow.org/api/latest/#setBackend)