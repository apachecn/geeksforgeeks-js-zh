# Tensorflow.js tf.removeBackend（） 函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-remove 后端函数/

[**Tensorflow.js**](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**TF . remove 后端()功能**用于删除后端和注册工厂。

**语法:**

```
tf.removeBackend(name) 
```

**参数:**

*   **名称:**我们要移除的后端的名称。

**返回值:**返回 void

**例 1:**

## Javascript

```
// Setting the backend
tf.setBackend("cpu")

console.log(tf.getBackend())

tf.removeBackend('cpu')

console.log(tf.getBackend())
```

**输出:**

```
cpu
null
```

**示例 2:** 在本例中，我们已经将后端设置为“cpu”，然后将其移除并设置为“webgl”。

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

**参考:**[https://js.tensorflow.org/api/latest/#removeBackend](https://js.tensorflow.org/api/latest/#removeBackend)