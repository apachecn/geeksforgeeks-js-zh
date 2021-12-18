# JavaScript type error–变数「x」重新宣告引数

> 原文:[https://www . geesforgeks . org/JavaScript-type error-variable-x-redclares-argument/](https://www.geeksforgeeks.org/javascript-typeerror-variable-x-redeclares-argument/)

这个 JavaScript 异常**变量重新声明参数**仅在严格模式下发生，如果变量名(也是函数参数)已经用**变量**关键字重新声明。

**消息:**T0】

**错误类型:**

```
TypeError

```

**错误原因:**作为函数参数的变量在函数内部用 var 关键字重新声明。

**示例 1:** 在本例中，变量(' varName ')已被重新声明。

## HTML

```
<script>
'use strict';
function fun(varName) { 
  var varName = 'This is GFG'; // Error Here 
}
</script>
```

**输出:**

```
TypeError: variable "varName" redeclares argument

```

**示例 2:** 在本例中，变量(' argName ')已被重新声明，函数也被调用。

## HTML

```
<script>
'use strict';
function fun2(argName) { 
  var argName = 'This is gfg'; // Error Here 
}
fun2('This is GeeksFooGeeks');
</script>
```

**输出:**

```
TypeError: variable "argName" redeclares argument

```