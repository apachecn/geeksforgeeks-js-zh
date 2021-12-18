# 是什么！！JavaScript 中的(不是不是)运算符？

> 原文:[https://www . geesforgeks . org/什么是 javascript 中的非非运算符/](https://www.geeksforgeeks.org/what-is-the-not-not-operator-in-javascript/)

**！！(不是不是)**是*一元逻辑运算符 not(！)两次*。双重否定(！！)运算符计算值的真值。该运算符返回一个布尔值，该值取决于给定表达式的真实性。
总的来说，顺理成章不(！)决定了一个价值不是什么的“真理”:

*   真相是假的不是真的(这就是原因！假结果为真)
*   真相是真的不是假的(这就是原因！真导致假)

！！决定了一个价值不是什么的“真理”:

*   真相是真的不是真的(这就是原因！！真结果为真)
*   真相是假的不是假的(这就是原因！！假结果导致假)

**示例-1:** 本示例检查布尔值 true 的真实性。

```
<script>
    // Write Javascript code here
    var n1;
    /* checking truthyness of
    the boolean value true. */
    n1 = !!true;
    document.write(n1);
</script>
```

**输出:**

```
true

```

**示例-2:** 本示例检查布尔值 false 的错误性。

```
<script>
    // Write Javascript code here
    var n1;
    // checking falsyness of the boolean value false. 
    n1 = !!false;
    document.write(n1);
</script>
```

**输出:**

```
false

```

**示例-3:** 本示例检查给定字符串的真假。

```
<script>
    // Write Javascript code here
    var n1;
    // checking the truthyness or falsyness of a given string.
    n1 = !!"Javascript programming";
    document.write(n1);
</script>
```

**输出:**

```
true

```

**示例-4:** 本示例检查给定对象的真假。

```
<script>
    // Write Javascript code here
    var n1;
    // checking the truthyness 
    // or falsyness of a given object.
    n1 = !!{
        articles: 70
    };
    document.write(n1);
</script>
```

**输出:**

```
true

```