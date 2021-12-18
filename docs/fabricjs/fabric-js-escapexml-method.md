# Fabric.js 擒纵 Xml()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-escapexml-method/](https://www.geeksforgeeks.org/fabric-js-escapexml-method/)

**转义 Xml()方法**用于转义指定字符串中的 XML 标记语言字符。

**语法:**

```
escapeXml(string)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **字符串:**此参数保存要转义的字符串。

**返回值:**这个方法返回指定字符串的转义版本。

**例 1:**

## java 描述语言

```
<!DOCTYPE html>

<html>

<head>
   <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js" >
   </script>

   <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js.map">
   </script>

   <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.js">
   </script>
</head>

<body>
   <script type="text/javascript">
        // Printing a string with the help
        // of escapeXml() function 
        // without the characters of XML
        console.log(fabric.util.string.escapeXml("GeeksforGeeks"));

        // Printing a string with the help
        // of escapeXml() function 
        // with the characters of XML
        console.log(fabric.util.string.escapeXml("Geeks<abc>for</abc>Geeks"));

        // Printing a string without the help
        // of escapeXml() function 
        // with the characters of XML
        console.log("Geeks<abc>for</abc>Geeks");
   </script>

</body>

</html>
```

**输出:**

```
GeeksforGeeks
Geeks<abc>for</abc>Geeks
GeeksforGeeks
```

**例 2:**

## java 描述语言

```
<!DOCTYPE html>

<html>

<head>
   <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js" >
   </script>

   <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js.map">
   </script>

   <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.js">
   </script>
</head>

<body>
   <script type="text/javascript">
        console.log("Using escapeXml() Function:");
        var value="GFG <a> is a CS </a> portal.";
        console.log(fabric.util.string.escapeXml(value));

        console.log("Without using escapeXml() Function:");
        var value="GFG <a> is a CS </a> portal.";
        console.log(value);
   </script>

</body>

</html>
```

**输出:**

```
Using escapeXml() Function:
GFG <a> is a CS </a> portal.
Without using escapeXml() Function:
GFG is a CS portal.
```