# 如何在 JavaScript 中用不同的方式声明变量？

> 原文:[https://www . geesforgeks . org/如何用 javascript 以不同方式声明变量/](https://www.geeksforgeeks.org/how-to-declare-variables-in-different-ways-in-javascript/)

在 JavaScript 中，我们可以使用不同的关键字以不同的方式声明一个变量。每个关键字在 JavaScript 中都包含一些特定的原因或特性。基本上我们可以通过使用 **var** 、 **let** 和 **const** 关键字以三种不同的方式来声明变量。每个关键字都在某些特定条件下使用。
**var:** 此关键字用于全局声明变量。如果你用这个关键字来声明变量，那么这个变量可以是全局可访问的，也是可变的。这对于短长度的代码来说是很好的，如果代码变得很大，那么你会感到困惑。

*   **语法:**

```
var variableName = "Variable-Value;"
```

*   **代码:**

## java 描述语言

```
<script>
    var geeks = "GeeksforGeeks";
    console.log(geeks);
</script>
```

*   **输出:**

```
GeeksforGeeks
```

**let:** 此关键字用于在本地声明变量。如果您使用这个关键字来声明变量，那么这个变量可以在本地访问，并且也是可变的。如果代码变得庞大，那就好了。

*   **语法:**

```
let variableName = "Variable-Value;"
```

*   **代码:**

## java 描述语言

```
<script>
if (true) {
    let geeks = "GeeksforGeeks";
    console.log(geeks);
    }

    /* This will be error and
       show geeks is not defined */
    console.log(geeks);
</script>
```

*   **输出:**

```
GeeksforGeeks
```

**const:** 此关键字用于全局声明变量。如果你用这个关键字来声明变量，那么这个变量是全局可访问的，它是不可改变的。

*   **语法:**

```
const variableName = "Variable-Value;"
```

*   **代码:**

## java 描述语言

```
<script>
    const geeks = "GeeksforGeeks";
    console.log(geeks);
</script>
```

*   **输出:**

```
GeeksforGeeks
```