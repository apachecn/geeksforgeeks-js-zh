# tensorflow . js TF . data . dataset 类。shuffle()方法

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-dataset-class-shuffle-method/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-dataset-class-shuffle-method/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**TF . data . dataset . shuffle()**方法沿着张量的第一维随机地对其进行 shuffle。

**语法:**

```
tf.data.Dataset.shuffle(
    buffer_size, seed=None, 
    reshuffle_each_iteration=None
)
```

**参数:**

*   **buffer_size:** 这是将从中采样新数据集的元素数量。
*   **种子【可选】:** 它是一个可选参数，用于创建一个随机种子进行分配，要看到相同的结果使用相同的种子。
*   **reshuffle _ each _ iteration:**一个布尔值，为 true 表示数据集每次迭代时都要进行伪随机重新洗牌。默认值为真。它是可选参数。

**返回值:** 一个形状和数据类型与值相同的张量，但沿其第一维方向混洗。

**示例 1:** 在本例中，我们首先创建一个张量，然后对其进行洗牌，在本例中***r*****eshuffle _ every _ iteration****为 True**

## **Javascript**

```
async function shuffle() {

    // Creating a Tensor
    const a = tf.data.array([1, 2, 3, 4, 5, 6]).shuffle(3);
    await a.forEachAsync(e => console.log(e)); //print 1
    await a.forEachAsync(e => console.log(e)); //print 2
}

shuffle();
```

****输出:****

```
**3 4 1 2 5 6**
**3 4 2 5 6 1**
```

****示例 2:** 在本例中， **seed** 被设置为 Integer，每当使用特定的整数时，它将生成该特定的输出**

## **Javascript**

```
async function shuffleseed() {
    const a = tf.data.array([1, 2, 3]).shuffle(3, seed = 42);
    await a.forEachAsync(e => console.log(e));

    const b = tf.data.array([1, 2, 3]).shuffle(3, seed = 42);
    await b.forEachAsync(e => console.log(e));
}

shuffleseed();
```

****输出:****

```
2 1 3
2 1 3
```

****参考:**[**https://js . tensorflow . org/API/3 . 6 . 0/# TF . data . dataset . shuffle**](https://js.tensorflow.org/api/3.6.0/#tf.data.Dataset.shuffle)**