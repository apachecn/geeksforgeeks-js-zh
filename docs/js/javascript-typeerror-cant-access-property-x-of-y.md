# JavaScript 类型错误–无法访问“Y”的属性“X”

> 原文:[https://www . geesforgeks . org/JavaScript-type error-cant-access-property-x-of-y/](https://www.geeksforgeeks.org/javascript-typeerror-cant-access-property-x-of-y/)

如果对未定义或空值执行属性访问，将出现此 JavaScript 异常**无法访问属性**。

**消息:**T0】

**例:**

```
TypeError: x is undefined, can't access property "prop" 
           of it 
TypeError: x is null, can't access property "prop" of it 
TypeError: can't access property "prop" of undefined
TypeError: can't access property "prop" of null
```

**错误类型:**

```
TypeError

```

**错误原因:**对代码中任何未定义或空值执行了属性访问。

**例 1:** 在本例中，GFG 是未定义的，因此出现了错误。

## HTML

```
<script>
    var GFG = undefined;
    GFG.substring(3); // error here
</script>
```

**输出(控制台):**

```
TypeError: Unable to get property 'substring' of undefined or null reference

```

**示例 2:** 在本例中，GFG 为空，因此出现了错误。

## HTML

```
<script>
    var GFG = null;
    GFG.substring(3); // error here
</script>
```

**输出(控制台):**

```
TypeError: Unable to get property 'substring' of undefined or null reference

```