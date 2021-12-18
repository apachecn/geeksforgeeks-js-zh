# 洛达什 _。isElement()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-iselement-method/](https://www.geeksforgeeks.org/lodash-_-iselement-method/)

洛达什 **_。isElement()方法**用于检查指定值是否为 DOM 元素。

**语法:**

```
_.isElement( value )
```

**参数:**该方法接受一个如上所述的参数，描述如下:

*   **Value:** This parameter holds the value to be checked.

**返回值:**如果指定的值是 DOM 元素，则该方法返回布尔值 true，否则返回 false。

**示例 1:**

## HTML

```
<html> 

<head> 
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/lodash.js/2.4.1/lodash.min.js">
    </script>
</head> 

<body> 
    <script type="text/javascript"> 
        console.log(_.isElement("gfg"));
        console.log(_.isElement(123)); 
    </script> 
</body> 

</html>
```

**输出:**

```
false
false

```

**示例 2:**

## HTML

```
<html> 

<head> 
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/lodash.js/2.4.1/lodash.min.js">
    </script>
</head> 

<body> 
    <script type="text/javascript"> 
        console.log(_.isElement(document.body));
    </script> 
</body> 

</html>
```

**输出:**

```
true

```

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装 lodash 库。