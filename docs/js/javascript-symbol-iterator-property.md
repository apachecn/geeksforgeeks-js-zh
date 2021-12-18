# JavaScript 符号.迭代器属性

> 原文:[https://www . geesforgeks . org/JavaScript-symbol-iterator-property/](https://www.geeksforgeeks.org/javascript-symbol-iterator-property/)

它是 [Iterables](https://www.geeksforgeeks.org/javascript-iterator/) 的一个对象，也是一种广义数组。使任何对象更容易在 for 中使用的表..循环的。我们知道数组本质上是迭代的，但除此之外，还有几个对象用于迭代目的。假设任何不是数组但拥有一组列表、集合等的对象..的可用于迭代它。

我们用于..表示任意区间的范围对象。它决定..的循环将工作并迭代循环。

我们将使用一个方法 symbol . iterator(JavaScript 中的内置方法)来迭代上面提到的 range 对象。该方法的工作步骤为:

1.  At the beginning of the first .. loop, it first checks for errors, and if no errors are found, it uses the method to access the methods and objects.

2.  To get the next upcoming value, it calls the next () method for the output object.
3.  The returned value is in the form of {done: Boolean, value: any}. When done=true returns, the loop will be treated as a complete loop.

**语法:**

```
[Symbol.iterator]
```

#### 特点:

*   该范围本身不会有 next()方法。
*   当我们调用范围【Symbol.iterator】()时，就形成了一个迭代器，下一个()方法将为进一步的迭代生成该值。

**例:**

## Javascript

```
let range = {
  from: 2,
  to: 7
};

range[Symbol.iterator] = function() {

  return {
    now: this.from,
    end: this.to,
    next() {
      if (this.now <= this.end) {
        return { done: false, value: this.now++ };
      } else {
        return { done: true };
      }
    }
  };
};

for (let i of range) {
  console.log(i); 
}
```

**输出:**

```
2
3
4
5
6
7
```