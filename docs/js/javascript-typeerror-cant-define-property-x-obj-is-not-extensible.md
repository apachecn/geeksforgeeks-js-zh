# JavaScript type error–无法定义属性“X”:“Obj”不可扩展

> 原文:[https://www . geesforgeks . org/JavaScript-type error-cant-define-property-x-obj-is-不可扩展/](https://www.geeksforgeeks.org/javascript-typeerror-cant-define-property-x-obj-is-not-extensible/)

这个 JavaScript 异常**不能定义属性“x”:“obj”是不可扩展的**发生在**object . preventextextensions()**用在一个对象上使其不再可扩展的时候，所以现在不能给对象添加新的属性。

**消息:**

```
TypeError: Cannot create property for a non-extensible object (Edge)
TypeError: can't define property "x": "obj" is not extensible (Firefox)
TypeError: Cannot define property: "x", object is not extensible. (Chrome)

```

**错误类型:**

```
TypeError

```

**错误原因:**在对象上应用 Object.preventExtensions()方法后，会向对象添加新属性，这是不允许的。

**示例 1:** 在本示例中，在应用了**object . preventextextensions()**方法后添加了新属性，因此出现了错误。

## 超文本标记语言

```
<script>
    'use strict';

    var GFG_Obj = {'name': 'GFG'};
    Object.preventExtensions(GFG_Obj);

    GFG_Obj.age = 22; // error here
</script>
```

**输出(控制台中):**

```
TypeError: Cannot create property for a non-extensible object

```

**示例 2:** 在本示例中，在应用了**object . preventetextures()**方法之后，正在使用 **defineProperty()** 方法添加新属性，因此出现了错误。

## 超文本标记语言

```
<script>
    'use strict';

    var GFG_Obj = {'name': 'GFG'};
    Object.preventExtensions(GFG_Obj);

    // error here
    Object.defineProperty(GFG_Obj, 
      'person', { dob: "02/11/1997" }
    );
</script>
```

**输出(控制台中):**

```
TypeError: Cannot define property 'person': object is not extensible

```