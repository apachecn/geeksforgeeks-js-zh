# 如果一个对象看起来像一个承诺

则返回真的 JavaScript 程序

> 原文:[https://www . geesforgeks . org/JavaScript-返回真的程序-如果一个对象看起来像一个承诺/](https://www.geeksforgeeks.org/javascript-program-that-returns-true-if-an-object-looks-like-a-promise/)

在 JavaScript 中，**承诺**是将生产代码和消费代码链接在一起的对象。简单来说，JavaScript 中的承诺和现实生活中的承诺是一样的。每当一个承诺被创造出来，有 3 个条件，或者说我们可以期待的结果:

*   解决
*   拒绝
*   悬而未决的

正如上面的名字所暗示的，每当一个承诺被创造出来，我们要么得到承诺的履行，即承诺被**解决**，要么如果我们没有得到预期的结果，即承诺没有得到履行，则是**拒绝**。承诺既没有被解决也没有被拒绝的状态称为**待定**。

**语法:**

```
var promise = new Promise(function(resolve, reject) {
    (the producing code)
});

```

在本文中，我们将确定一个 JavaScript 对象是否是 Promise。现在有很多方法可以识别相同的东西，让我们看看它们是什么，以及我们如何轻松识别承诺。

**进场:**

*   取一组变量和对象。
*   将这些值传递给一个函数 isPromise()，该函数实际上检查不同的条件并识别一个承诺。

**方法 1:** 使用运算符的**类型:**

## java 描述语言

```
<script>

    //Checking for a promise
    var prom = new Promise(function(resolve, reject) {
        resolve();
    });

    var num = 10;
    var name = "geeksforgeeks";
    var object = {
        site: "geeksforgeeks"
    };

    console.log(isPromise(prom));
    console.log(isPromise(num));
    console.log(isPromise(name));
    console.log(isPromise(object));

    function isPromise(p) {
        return Boolean(p && 
            typeof p.then === "function");
    }
</script>
```

**输出:**

```
true
false
false
false
```

**方法 2:** 通过检查传递的值 p 是否是一个**对象**并检查 p.then 是否是一个**函数。**

## java 描述语言

```
<script>

    // Checking for a promise
    var prom = new Promise(function(resolve, reject) {
        resolve();
    });
    var num = 10;
    var name = "geeksforgeeks";
    var object = {
        site: "geeksforgeeks"
    };

    console.log(isPromise(prom));
    console.log(isPromise(num));
    console.log(isPromise(name));
    console.log(isPromise(object));

    function isPromise(p) {
        return !!p && (typeof p === 'object' 
            || typeof p === 'function') 
            && typeof p.then === 'function';
    }
</script>
```

**输出:**

```
true
false
false
false
```

**方法 3:** 通过检查**是否承诺.解决(p) == p:**

## java 描述语言

```
<script>

    // Checking for a promise
    var prom = new Promise(function(resolve, reject) {
        resolve();
    });

    var num = 10;
    var name = "geeksforgeeks";
    var object = {
        site: "geeksforgeeks"
    };

    console.log(isPromise(prom));
    console.log(isPromise(num));
    console.log(isPromise(name));
    console.log(isPromise(object));

    function isPromise(p) {
        if (Promise && Promise.resolve) {
            return Promise.resolve(p) == p;
        }
    }
</script>
```

**输出:**

```
true
false
false
false
```