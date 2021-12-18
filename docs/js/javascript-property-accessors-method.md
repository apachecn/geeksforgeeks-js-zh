# JavaScript 属性访问器方法

> 原文:[https://www . geesforgeks . org/JavaScript-property-accessors-method/](https://www.geeksforgeeks.org/javascript-property-accessors-method/)

属性访问器允许使用对象的属性名或键进行访问(读取、创建、更新)。

JavaScript 中有两种符号允许我们访问对象的属性:

*   Point symbol
*   Bracket symbol []

如果对象没有找到匹配的键(或属性名或方法名)，属性访问器将返回 undefined。

**点符号**

在*对象.属性*语法中，属性必须具有有效的 JavaScript 标识符。(作为 ECMAScript 标准的一部分，属性名称是技术性的“标识名称”，而不是“标识符”，因此使用了保留字，但不推荐使用)。

> object _ name . property _ name；

**例:**

## Javascript

```
<script>
  const obj = {
   g: 'geeks',
   fg: 'forgeeks'
  };
  console.log(obj.g)
</script>
```

**输出:**

> **极客**

**括号符号**

表达式是解析/评估值的有效代码单元。然后，解析值被类型化为字符串，该字符串被视为属性名。

注意:任何作为关键字的 property_name 都不能被访问，因为它会给你一个意外的标记错误。

> object _ name[表达式]；
> 
> T3】

**例:**

## Javascript

```
const obj = {
 g: 'geeks',
 fg: 'forgeeks'
};
console.log(obj['fg'])
```

**输出:**

> **锻造**