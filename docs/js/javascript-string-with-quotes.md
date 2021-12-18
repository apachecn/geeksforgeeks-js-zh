# 带引号的 JavaScript 字符串

> 原文:[https://www . geesforgeks . org/JavaScript-带引号的字符串/](https://www.geeksforgeeks.org/javascript-string-with-quotes/)

[字符串](https://www.geeksforgeeks.org/javascript-strings/)是字符、符号和数字的序列。在 JavaScript 中，用户可以用“*单引号*或“*双引号*来编写字符串。但是，两者都在终端上打印相同的结果。

```
'GeeksforGeeks' === "GeeksforGeeks"
```

在某些情况下，用户可能需要打印字符串中带有引号的部分。比如我是，你好“极客”，或者是苹果等。在这种情况下，用户必须谨慎使用单引号和双引号。在本教程中，用户将学习用引号将字符串写出来。

**简单字符串在 JavaScript 中是如何工作的？**

如上节所述，用户要么用单引号或双引号写入字符串，要么得到相同的输出。用户可以看到下面的示例代码。

**示例:**

## java 描述语言

```
<script>
// String with double quotes
var string1 = "Hello Geeks!!!"

// String with single quotes
var string2 = 'You are on GeeksforGeeks!'

console.log(string1)
console.log(string2)
</script>
```

**输出:**

```
Hello Geeks!!!
You are on GeeksforGeeks!
```

**用户如何在字符串中添加引号？**

有几种方法可以写出带引号的字符串。

**方法 1:** 可以使用字符串内部的反斜杠(\)来转义引号。他们将需要遵循下面的例子来遵循这个方法。

**语法:**

```
var string = "I\'m user of GeeksForGeeks."
```

**示例:**

## java 描述语言

```
<script>
var string1 = "I\'m user of GeeksForGeeks."
var string2 = 'I\'m user of GeeksForGeeks.'
var string3 = 'Hello \'Geeks\''
var string4 = "Hello \'Geeks\'"

console.log(string1)
console.log(string2)
console.log(string3)
console.log(string4)
</script>
```

**输出:**

```
I'm user of GeeksForGeeks.
I'm user of GeeksForGeeks.
Hello 'Geeks'
Hello 'Geeks'
```

**方法 2:** 可以使用替代引号编写字符串。如果用户将字符串写成双引号，则需要在字符串中使用单引号，反之亦然。

**语法:**

```
var string1 = "Hello 'Geeks'"
var strign2 = 'Hello "Geeks"'
```

**示例:**

## java 描述语言

```
<script>
var string1 = "I'm user of GeeksForGeeks."
var string2 = 'I"m user of GeeksForGeeks.'
var string3 = 'Hello "Geeks"'
var string4 = "Hello 'Geeks'"

console.log(string1)
console.log(string2)
console.log(string3)
console.log(string4)
</script>
```

**输出:**

```
I'm user of GeeksForGeeks."
I"m user of GeeksForGeeks.'
Hello "Geeks"
Hello 'Geeks'
```