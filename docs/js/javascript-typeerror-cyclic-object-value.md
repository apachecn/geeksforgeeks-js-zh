# JavaScript 类型错误–循环对象值

> 原文:[https://www . geesforgeks . org/JavaScript-type error-cyclic-object-value/](https://www.geeksforgeeks.org/javascript-typeerror-cyclic-object-value/)

如果在 JSON 中找到对象的引用，就会出现这个 JavaScript 异常**循环对象值**。JSON.stringify()无法解决它们。

**消息:**T0】

**错误类型:**

```
TypeError

```

**错误原因:**如果在代码中找到引用，那么 JSON.stringify()无法解决它们。

**示例 1:** 在本例中，circObj 引用了自身，因此出现了错误。

## HTML

```
<script>
    var circObj = {1: "1"};
    circObj.myself = circObj;
    JSON.stringify(circObj);
</script>
```

**输出:**

```
TypeError: Converting circular structure to JSON

```

**例 2:** 在这个例子中，GFG_Obj 有一个对自身的引用，JSON.stringify()无法求解。所以错误发生了。

## HTML

```
<script>
    var GFG_Obj = {property_1: "value_1"};
    GFG_Obj.myself = GFG_Obj;
    JSON.stringify(GFG_Obj);
</script>
```

**输出:**

```
TypeError: Converting circular structure to JSON

```