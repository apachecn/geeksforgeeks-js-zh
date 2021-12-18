# JavaScript 中 unescape()和 escape()函数的区别

> 原文:[https://www . geesforgeks . org/unescape-和-escape-functions-in-JavaScript/](https://www.geeksforgeeks.org/difference-between-unescape-and-escape-functions-in-javascript/)之间的区别

在本文中，我们将学习 JavaScript 中的 escape() & unescape()函数。我们将通过示例了解使用这两个函数的目的。在本文的后面，我们将讨论 escape() & unescape()函数之间的区别。让我们讨论 escape()函数。

**1。escape()函数:**该函数将字符串作为单个参数&对可以通过支持 ASCII 字符的计算机网络传输的字符串进行编码。**编码**是将明文转换为密文的过程。

**语法:**

```
escape( string )
```

**参数:**该函数接受单个参数:

*   **字符串:**该参数保存将要编码的字符串。

**返回值:**返回编码字符串。

**注意:**escape()函数只对特殊字符进行编码，此函数不推荐使用。

**异常:**@–+。/ * _

**示例:**在本例中，我们使用了特殊字符来查看变化。

## java 描述语言

```
<script>
   // Special character encoded with escape function
   document.write(escape("Geeks for Geeks!!!"));

   document.write("<br>");

   // Print encoded string using escape() function
   // Also include exceptions i.e. @ and .
   document.write(escape("To contribute articles contact"+
                       " us at contribute@geeksforgeeks.org"));
</script>

```

**输出:**

```
Geeks%20for%20Geeks%21%21%21
To%20contribute%20articles%20contact%20us%20atcontribute
@geeksforgeeks.org 
```

从上面的输出中，我们可以看到带有特殊符号“@”的电子邮件地址中的异常没有被编码&显示与输入中相同&其余的文本被编码。

如果我们想转换编码文本。，密文变成正常可读的文本那么我们就不得不使用 **unescape()** 函数来解码编码的文本。**解码**是将密文转换为明文的过程。

**2。unescape()函数:**该函数将字符串作为单个参数，并使用它对 escape()函数编码的字符串进行解码。当通过 unescape()函数解码时，字符串中的十六进制序列将被它们所代表的字符替换。

**语法:**

```
unescape(string)
```

**参数:**该函数接受单个参数:

*   **字符串:**此参数保存将被解码的字符串。

**返回值:**返回解码后的字符串。

**注意:**此功能只解码特殊字符，此功能已弃用。

**异常:**@–+。/ * _

**例 1:** 在本例中，我们使用了特殊字符来查看变化。

## java 描述语言

```
<script>
   // Special character encoded with escape function
   document.write(unescape("Geeks%20for%20Geeks%21%21%21"));

   document.write("<br>");

   // Print encoded string using escape() function
   // Also include exceptions i.e. @ and .
   document.write(unescape("To%20contribute%20articles%20contact"+
                   "%20us%20atcontribute@geeksforgeeks.org"));
</script>

```

**输出:**

```
Geeks for Geeks!!!
To contribute articles contact us at  
contribute@geeksforgeeks.org
```

从上面的例子中，我们可以看到密文通过使用 unescape()函数被解码为纯文本。

**例 2:**

## java 描述语言

```
<script>
   // Special character encoded with escape function
   var str = escape("Geeks for Geeks!!!");
   document.write("Encoded : " + str);

   // New Line
   document.write("<br>");

   // unescape() function
   document.write("Decoded : " + unescape(str))

   // New Line
   document.write("<br><br>");

   // The exception
   // @ and . not encoded.
   str = escape("To contribute articles contact us" +
                   "at contribute@geeksforgeeks.org")
   document.write("Encoded : " + str);

   // New Line
   document.write("<br>");

   // unescape() function
   document.write("Decoded : " + unescape(str))
</script>
```

**输出:**

```
Encoded : Geeks%20for%20Geeks%21%21%21
Decoded : Geeks for Geeks!!!

Encoded : To%20contribute%20articles%20contact%20us%20
          at%20contribute@geeksforgeeks.org
Decoded : To contribute articles contact us at 
          contribute@geeksforgeeks.org
```

**unescape()&escape()函数的区别:**

<figure class="table">

|  | 

#### 联合国教科文组织()T3

 | 

#### **【逃()**

 |
| --- | --- | --- |
| 1。 | unescape()函数用于解码由 escape()函数编码的字符串。 | JavaScript 中的 escape()函数用于对字符串进行编码。使用 ASCII 字符支持，它使字符串可移植，因此它可以通过任何网络传输到任何计算机。 |
| 2。 | 返回解码后的字符串。 | 返回一个编码字符串。 |
| 3。 | 此功能仅编码特殊字符，此功能已弃用。有一定的例外:@–+。/ * _ | 此功能只对特殊字符进行编码，此功能已弃用。有一定的例外:@–+。/* _ |

</figure>