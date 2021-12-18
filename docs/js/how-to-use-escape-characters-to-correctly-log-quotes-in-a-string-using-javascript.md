# 如何使用 JavaScript 使用转义字符正确记录字符串中的引号？

> 原文:[https://www . geeksforgeeks . org/如何使用转义字符正确记录字符串引号使用 javascript/](https://www.geeksforgeeks.org/how-to-use-escape-characters-to-correctly-log-quotes-in-a-string-using-javascript/)

**转义**字符是用于开始转义命令以执行某些操作的符号。他们是可以用不同于我们意图的方式来解释的角色。Javascript 在前面使用“ **\** ”(反斜杠)作为转义字符。

我们的目标是希望在控制台中打印，如:

```
""Geeks" for "Geeks" is 'the' best 'platform'"
```

要打印报价，使用转义字符，我们有两个选项:

*   单引号: **\'** *(反斜杠后跟单引号)*
*   双引号:**\***(反斜杠后加双引号)*

我们可以在控制台中使用单引号和双引号打印引号，而不使用转义字符。但是有一个限制，我们可以只打印单引号或双引号。如果字符串用单引号表示，那么我们可以只打印双引号，如果字符串用单引号表示，那么我们可以在其中打印双引号。*单引号或双引号表示的字符串相同，没有区别*。

## java 描述语言

```
<script>

    // Using single quotes for string
    let s1 = 'Geeks for Geeks';

    // Using double quotes for string
    let s2 = "Geeks for Geeks";

    // Both s1 and s2 are same
    console.log((s1 === s2)); // true
    console.log(s1); // Geeks for Geeks
    console.log(s2); // Geeks for Geeks

    // Using single quotes to represent string
    // and double to represent quotes inside
    // string
    let str = '"Geeks" "FOR" Geeks';
    console.log(str); // "Geeks" "FOR" Geeks

    // Using double quotes to represent string
    // and single to represent quotes in string
    str = "'Geeks' 'FOR' Geeks";
    console.log(str); // 'Geeks' 'FOR' Geeks
</script>
```

**输出:**

```
true
Geeks for Geeks
Geeks for Geeks
"Geeks" "FOR" Geeks
'Geeks' 'FOR' Geeks
```

**示例 2:** 使用转义序列–如果您已经用“’开始引号，那么您必须用“’结束引号，反之亦然。

## java 描述语言

```
<script>

    // Using escape sequences - here you can
    // use single as well as double quotes
    // within the string to print quotation
    let str = 'Geeks \'FOR\' Geeks';
    console.log(str); // Geeks 'FOR' Geeks

    str = "Geeks \"FOR\" Geeks";
    console.log(str); // Geeks "FOR" Geeks

    str = '\'Geeks \"FOR\" Geeks\'';
    console.log(str); // 'Geeks "FOR" Geeks'

    str = "\"\"Geeks\" for \"Geeks\" is \'the\' best \'platform\'\"";
    console.log(str); // ""Geeks" for "Geeks" is 'the' best 'platform'"
</script>
```

***输出:***

```
Geeks 'FOR' Geeks
Geeks "FOR" Geeks
'Geeks "FOR" Geeks'
""Geeks" for "Geeks" is 'the' best 'platform'"
```