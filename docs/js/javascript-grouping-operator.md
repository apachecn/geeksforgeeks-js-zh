# JavaScript 分组运算符

> 原文:[https://www.geeksforgeeks.org/javascript-grouping-operator/](https://www.geeksforgeeks.org/javascript-grouping-operator/)

下面是分组运算符的示例。

*   **例:**

## jscript

```
<script>
    function gfg() {
     // 3 * (2 + 3)
    let value1= 3 * (2 + 3);
         // (3 + 2) * 3
    let value2= (3 + 2) * 3;
    document.write(value1 + "</br>" + value2);
    }
    gfg();
</script>                   
```

*   **输出:**

```
15
15
```

**分组运算符**由表达式或子表达式周围的一对圆括号组成，用于覆盖正常的运算符优先级，以便优先级较低的表达式可以在优先级较高的表达式之前求值。此运算符只能包含表达式。参数列表被传递给该运算符内的函数，该函数将它视为表达式。
**语法:**

```
( )
```

这个**()运算符**控制表达式
中求值的优先顺序。下面的例子说明了 JavaScript 中的分组运算符:
**例子 1:** 作为语句和异常的功能。在下面的代码中，如果函数前面没有任何其他语句，JavaScript 会将其视为语句。但是应用比任何其他运算符优先级最高的分组运算符会将该函数视为表达式，因此会对其进行完全求值。

## Java Script 语言

```
<script>
    function(x){ return x };
    // SyntaxError: Function statements
    // require a function name.

    // function as expression
    (function(x){ return x });
    // This will run without any exception.
</script>                   
```

**例 2:** 有无分组运算符。

## jscript

```
<script>
    function gfg() {
    // 5 * 5 + 5
    // 25+5
    // 30
    let value= 5 * 5 + 5 ;
    document.write("Without grouping operator: " + value);

    // 5 * (5 + 5)
    // 5*10
    // 50
    let value1= 5 * (5 + 5);
    document.write("</br>With grouping operator: "+ value1);
    }
    gfg();
</script>                   
```

**输出:**

```
Without grouping operator: 30
With grouping operator: 50
```

**支持的浏览器:**

*   Chrome 1 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 3 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上