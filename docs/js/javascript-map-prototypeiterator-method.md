# JavaScript Map . prototype[@ @迭代器]()方法

> 原文:[https://www . geeksforgeeks . org/JavaScript-map-prototypeeiterator-method/](https://www.geeksforgeeks.org/javascript-map-prototypeiterator-method/)

**Map[@ @迭代器]( )** 方法用于使 [Map](https://www.geeksforgeeks.org/map-in-javascript/) 可迭代。**Map[@ @迭代器]( )** 方法返回迭代器对象，该对象遍历 Map 的所有代码点。**映射[@ @迭代器]( )** 是**映射**的内置属性。

我们可以通过创建**地图** [迭代器](https://www.geeksforgeeks.org/javascript-iterator/)来使用这个方法。我们可以通过调用*@ @迭代器*属性来制作**映射**迭代器。代替*@ @迭代器*，我们可以使用 [Symbol.iterator](https://www.geeksforgeeks.org/javascript-symbol-iterator-property/) 常量。

**语法:**

```
const iter = Map[ Symbol.iterator](); 
```

**参数:**该属性不接受任何参数。
**返回值:**它返回一个迭代器来迭代迭代器对象的代码点。

**示例:**

## Java Script 语言

```
<script>
    const m = new Map();
    m.set(0, "a")
    m.set(2, "b")
    m.set(3, "c")
    const iterator = m[Symbol.iterator]();
    let itr = iterator.next()
    for (let i = 0; i < script m.size; i++) {
        console.log(itr.value, itr.done)
        itr = iterator.next()
    }
</script>
```

**输出:**

```
[0 : 'a'] false

[1 : 'b'] false

[2 : 'c'] false
```

**示例:**我们可以使用**Map . prototype 【@ @迭代器】**方法，将 **Map** 分配给迭代器。我们可以使用[](https://www.geeksforgeeks.org/javascript-for-loop/)*循环迭代地图的代码点。 *for-of* 循环使用迭代器来迭代映射的值。*

## *java 描述语言*

```
*<script>
    const m = new Map();
    m.set(0, "a")
    m.set(2, "b")
    m.set(3, "c")

    const iterator = m[Symbol.iterator]();

    let itr = iterator.next()

    for (let i = 0; i < m.size; i++) {

        console.log(itr.value)
        itr = iterator.next()

    }

    console.log("iterating with for-of loop : ")

    for (let i of m) {
        console.log(i)
    }
</script>*
```

***输出:***

```
*[0 : 'a']
[1 : 'b']
[2 : 'c']
iterating with for-of loop :
[0 : 'a']
[1 : 'b']
[2 : 'c']*
```