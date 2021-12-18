# JavaScript type error–不能使用“in”运算符在“Y”中搜索“X”

> 原文:[https://www . geesforgeks . org/JavaScript-type error-无法使用 in-operator-to-search-for-x-in-y/](https://www.geeksforgeeks.org/javascript-typeerror-cannot-use-in-operator-to-search-for-x-in-y/)

如果使用运算符中的**搜索字符串、数字或其他基本类型，则会出现此 JavaScript 异常**无法使用“in”运算符在“Y”**中搜索“X”。除了类型检查，它不能被使用。**

**消息:**

> 类型错误:对“in”(Edge)
> 的操作数无效类型错误:“in”的右侧必须是一个对象，得到了“x”(火狐)
> 类型错误:不能使用“in”运算符搜索“y”中的“x”(火狐，Chrome)

**错误类型:**

```
TypeError
```

**错误原因:**运算符中的**只能用于检查对象中是否有属性。这不能用于字符串、数字或其他基本类型的搜索。**

**例 1: in 运算符**不能用于字符串搜索，因此出现了错误。

## 超文本标记语言

```
<script>
"Geek" in "GeeksForGeeks"; // error here
</script>
```

**输出:**

```
TypeError: Invalid operand to 'in'

```

**例 2: in 运算符**不能用于字符串搜索，因此出现了错误。

## 超文本标记语言

```
<script>
var gfg = null;
"Geek" in gfg; // error here
</script>
```

**输出:**

```
TypeError: Invalid operand to 'in'

```