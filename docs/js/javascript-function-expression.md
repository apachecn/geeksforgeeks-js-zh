# JavaScript |函数表达式

> 原文:[https://www . geesforgeks . org/JavaScript-函数-表达式/](https://www.geeksforgeeks.org/javascript-function-expression/)

**函数表达式**允许我们创建一个没有任何函数名的匿名函数，这是函数表达式和函数声明的主要区别。函数表达式可以用作[life(立即调用的函数表达式)](https://www.geeksforgeeks.org/javascript-immediately-invoked-function-expressions-iife/)，它一被定义就运行。函数表达式必须存储在变量中，并且可以使用*变量名称进行访问。*随着 ES6 特性引入[箭头函数](https://www.geeksforgeeks.org/arrow-functions-in-javascript/)，声明函数表达式变得更加容易。

**函数声明语法:**

```
function *functionName(x, y)* { *statements...* return *(z)* };
```

**函数表达式语法(匿名):**

```
let *variableName* = function*(x, y)* { *statements...* return *(z)* };
```

**函数表达式语法(命名):**

```
let *variableName* = function *functionName(x, y)* 
{ *statements...* return *(z)* };
```

**箭头函数语法:**

```
let *variableName* = *(x, y)* => { *statements...* return *(z)* };
```

**注:**

*   在调用函数表达式或将其用作参数之前，必须先定义函数表达式。
*   箭头函数必须有 return 语句。

以下示例说明了 JavaScript 中的函数表达式:

**例 1:** 函数声明代码。

## java 描述语言

```
<script>
    function callAdd(x, y){
        let z = x + y;
        return z;   
    }
    console.log("Addition : " + callAdd(7, 4));
</script>
```

**输出:**

```
Addition : 11
```

**例 2:** 代码为功能表达式 **(** 匿名 **)**

## java 描述语言

```
<script>
    var calSub = function(x, y){
        let z = x - y;
        return z;
    }

    console.log("Subtraction : " + calSub(7, 4));
 </script>
```

**输出:**

```
Subtraction : 3
```

**例 3:** 代码为功能表达 **(** 命名为 **)**

## java 描述语言

```
<script>
    var calMul = function Mul(x, y){
        let z = x * y;
        return z;
    }

    console.log("Multiplication : " + calMul(7, 4));
</script>
```

**输出:**

```
Multiplication : 28
```

**例 4:** 代码为箭头功能

## java 描述语言

```
<script>
    var calDiv = (x, y) => {
        let z = x / y;
        return z;
    }

    console.log("Division : " + calDiv(24, 4));
</script>
```

**输出:**

```
Division : 6
```

**支持的浏览器:**

*   Chrome 1 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 3 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上