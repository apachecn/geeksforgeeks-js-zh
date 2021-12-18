# JavaScript 中单引号和双引号字符串的区别

> 原文:[https://www . geesforgeks . org/JavaScript 中单引号和双引号字符串的区别/](https://www.geeksforgeeks.org/difference-between-single-quoted-and-double-quoted-strings-in-javascript/)

[**JavaScript 中的**单引号**和**双引号**字符串都用于创建字符串文字。但是，当需要转义的字符本身是单引号或双引号字符串时，它们之间的基本区别就起作用了。当使用反斜杠(\)将文字括在单个代码中时，您需要转义单引号，或者当使用反斜杠(\)将文字括在双代码中时，您需要转义双引号。
。
**使用单引号字符串:**在使用单引号字符串定义字符串文字时，我们只需要转义字符串内部的单引号。而无需转义双引号，可以精确书写。**](https://www.geeksforgeeks.org/javascript-tutorial/)

**示例:**

## java 描述语言

```
<script>
    const geeks = 'We will visit \'GeeksforGeeks\' student.';
    const hello = 'Hello, I am an "Engineer"';
    document.write(geeks + "<br>");
    document.write(hello)
</script>    
```

**输出:**在这个例子中，GeeksforGeeks 必须写在单引号内。因为在定义字符串文字时，我们使用的是单引号字符串，所以我们需要在字符串中使用反斜杠(\)来转义单引号(')。工程师是用双引号引起来的。由于定义字符串文字时，我们使用的是单引号字符串，因此，我们不需要在字符串中转义双引号(" ")。

```
We will visit 'GeeksforGeeks' student.
Hello, I am an "Engineer"

```

**使用双引号字符串:**在使用双引号字符串定义字符串文字时，我们只需要转义字符串内部的双引号。虽然不需要转义单引号，并且可以精确书写。
T3】例:

## java 描述语言

```
<script>
    const geeks = "We will visit \"GeeksforGeeks\" student."
    const hello = "Hello, I am an 'Engineer'"
    document.write(geeks+"<br>")
    document.write(hello)
</script>    
```

**输出:**在本例中，GeeksforGeeks 必须用双引号括起来。因为在定义字符串文字时，我们使用的是双引号字符串，所以我们需要在字符串中使用反斜杠(\)来转义双引号(" ")。工程师用单引号括起来。由于定义字符串文字时，我们使用的是双引号字符串，因此，我们不需要在字符串中转义单引号(")。

```
We will visit "GeeksforGeeks" student.
Hello, I am an 'Engineer'

```

无论字符串用单引号还是双引号括起来，除了转义字符的行为之外，它们的行为方式完全相同。这意味着单引号中包含的字符串等于双引号中包含的字符串，前提是对必要的字符进行转义。

```
'GeeksforGeeks' === "GeeksforGeeks" 

```

*   **例 1:** 这里，我们已经声明了两个常数，即 a 和 b。在这两个常数中，我们存储了相同的文字 GeeksforGeeks，但是它们的封闭方式不同。常量 a 中的文字用双引号引起来，而常量 b 中的文字用单引号引起来。然后我们用三倍等号(===)比较常数 a 和 b，然后写出它的输出。这里，a===b 将比较存储在常数 a 和 b 中的字符串，如果它们严格且完全相等，将返回 true。如果不相等，将返回 false。在这里，输出为真意味着无论字符串是包含在单引号还是双引号中，它们都严格且完全等于相同的值。这仅仅意味着双引号或单引号不会影响括起来的字符串。

## java 描述语言

```
<script>
    const a = "GeeksforGeeks"
    const b = 'GeeksforGeeks'
    document.write(a===b)
</script>    
```

**输出:**

```
true

```

*   **示例 2:** 使用**反义词**或**发音符号(`)**是使用单引号或双引号的替代方法。在这种情况下，您不需要转义任何单引号或双引号。所以，这是一个没有错误的选择。同样，用 back-tic 括起来的字符串将严格且精确地等于用单引号或双引号括起来的字符串。

## java 描述语言

```
<script>
    const geeks = `We will visit "GeeksforGeeks" student.`
    const hello = `Hello, I am an 'Engineer'`
    document.write(geeks+"<br>")
    document.write(hello)
</script>    
```

**输出:**在这里，您可以看到，当我们在 back-tic(`)中封装字符串时，我们没有转义任何双引号或单引号，这为我们产生了相同的输出。

```
We will visit "GeeksforGeeks" student.
Hello, I am an 'Engineer'

```

**要记住的几点:**虽然 back-tic(`)可以在任何地方使用，并且错误更少，但是当从 JavaScript 中处理 **JSON** 文件时， **stringify()** 和 **parse()** 函数必须只包含在双引号中，因为它已经知道了双引号。

**在双引号和单引号中，哪一个更好:**两个引号都可以用在任何地方，但是你必须考虑需要转义的字符。

*   当你必须在字符串内写双引号(")时，最好选择单引号字符串，或者即使你选择的是双引号字符串，也不要忘记转义字符串内的双引号。
*   当您必须在字符串内写单引号(')时，最好选择双引号字符串，或者即使您选择单引号字符串，也不要忘记转义字符串内的单引号。
*   虽然您可以在上述两种情况下使用 back-tics(` ),但您不需要逃避任何事情。