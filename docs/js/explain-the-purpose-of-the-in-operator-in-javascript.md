# 解释 JavaScript 中“in”运算符的用途

> 原文:[https://www . geesforgeks . org/explain-in-operator-in-JavaScript 的用途/](https://www.geeksforgeeks.org/explain-the-purpose-of-the-in-operator-in-javascript/)

在本文中，我们将讨论在 [JavaScript 中可用的**操作符**中的**。**](https://www.geeksforgeeks.org/javascript-tutorial/)运算符中的**用于检查数据是在[对象](https://www.geeksforgeeks.org/objects-in-javascript/)内还是在[数组中。](https://www.geeksforgeeks.org/arrays-in-javascript/)在对象中，操作符中的*只作用于对象的键或属性。如果密钥或属性存在，则该操作符返回*真*否则*假。*类似地，对于数组，如果我们传递元素的索引而不是特定的值，它将返回 true。***

以下示例将帮助您理解运算符的用法。

**示例 1:** 使用运算符中的*处理对象。让我们首先创建一个对象，为了创建一个对象，我们必须分配键值对。*

```
const object = {
    User: 'Geek',
    Website: 'GeeksforGeeks',
    Language: 'JavaScript'
};
```

我们将通过使用操作符中的*来检查该键是否存在于对象中。*

## Java Script 语言

```
<script>
    const object = {
        User: 'Geek',
        Website: 'GeeksforGeeks',
        Language: 'JavaScript',
    };

    if ('User' in object) {
        document.write("Found");
    }
    else {
        document.write("Not found");
    }
</script>
```

**输出:**我们已经检查了‘用户’键是否在对象中，如果在对象中，则打印“找到”，否则打印“未找到”。

```
Found
```

**示例 2:** 使用带数组的运算符中的*。让我们先创建一个数组，要创建一个数组，我们必须给方括号中的数组赋值。*

```
const array1 = ["Geek", "GeeksforGeeks", "JavaScript"];
```

我们将检查数组中是否存在索引值，

## Java Script 语言

```
<script>
    const array1 = ["Geek", "GeeksforGeeks", "JavaScript"];
    if (1 in array1) {
        document.write("Found: ", array1[1]);
    }
    else {
        document.write("Not found");
    }
</script>
```

**输出:**我们已经检查了数组中是否存在索引 1。

```
Found: GeksforGeeks
```