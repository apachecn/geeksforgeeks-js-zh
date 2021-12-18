# JavaScript 布尔

> 原文:[https://www.geeksforgeeks.org/javascript-boolean/](https://www.geeksforgeeks.org/javascript-boolean/)

下面是 **JavaScript 布尔**方法的例子。

*   **例:**

## java 描述语言

```
<script>
    function gfg() {
document.write(Boolean(12));
    }
    gfg();
</script>
```

*   **输出:**

```
true
```

布尔是一种数据类型，它返回两个值中的一个，即真或假。在 JavaScript 中，布尔被用作获取变量、对象、条件、表达式等的值的函数。就真假而言。
**例:**
这里 a1 和 a2 分别存储布尔值即真和假。

```
var a1 = true;
var a2 = false;
```

**注意:**下面的变量是用字符串而不是布尔值初始化的。

```
var a1 ="true";
var a2 ="false";
```

**JavaScript 中的布尔()函数:**布尔函数返回变量的布尔值。它还可以用来查找条件、表达式等的布尔结果。
**语法:**

```
Boolean(variable/expression) 
```

**注意:**有值的变量或对象被视为**真**布尔值。0 '，' NaN '，空字符串，' undefined '，' null '被视为**假**布尔值。
**JavaScript 显示布尔值的工作方式**
**代码#1:**
下面程序会给出真值作为输出。

## java 描述语言

```
<!DOCTYPE html>
<html>
  <body>
     <script>
        document.write('Boolean(10) is ' + Boolean(10));
        document.write('<br>');
        document.write('Boolean("GeeksforGeeks") is '
              + Boolean("GeeksforGeeks"));
        document.write('<br>');
        document.write('Boolean(2.74) is ' + Boolean(2.74));
        document.write('<br>');
        document.write('Boolean(-1) is ' + Boolean(-1));
        document.write('<br>');
        document.write("Boolean('true') is " + Boolean('true'));
        document.write('<br>');
        document.write("Boolean('false') is " + Boolean('false'));
        document.write('<br>');
        document.write('Boolean(3 * 2 + 1.11) is '
              + Boolean(3 * 2 + 1.11));
        document.write('<br>');
        document.write('Boolean(1<2) is ' + Boolean(1 < 2));

     </script>
  </body>
</html>   
```

**输出:**

```
Boolean(10) is true
Boolean("GeeksforGeeks") is true
Boolean(2.74) is true
Boolean(-1) is true
Boolean('true') is true
Boolean('false') is true
Boolean(3 * 2 + 1.11) is true
Boolean(1<2) is true
```

**代码#2:**
下面的程序会给出假值作为输出。

## java 描述语言

```
<!DOCTYPE html>
<html>

<body>
    <script>
        var e; //undefined
        document.write('Boolean(0) is ' + Boolean(0));
        document.write('<br>');
        document.write('Boolean("") is ' + Boolean(""));
        document.write('<br>');
        document.write('Boolean(e) undefined is '
                   + Boolean(e));
        document.write('<br>');
        document.write('Boolean(-0) is ' + Boolean(-0));
        document.write('<br>');
        document.write('Boolean(false) is ' + Boolean(false));
        document.write('<br>');
        document.write('Boolean(NaN) is ' + Boolean(NaN));
        document.write('<br>');
        document.write('Boolean(null) is ' + Boolean(null));
        document.write('<br>');
        document.write('Boolean(1>2) is ' + Boolean(1 > 2));
    </script>
</body>

</html>            
```

**输出:**

```
Boolean(0) is false
Boolean("") is false
Boolean(e) undefined is false
Boolean(-0) is false
Boolean(false) is false
Boolean(NaN) is false
Boolean(null) is false
Boolean(1>2) is false
```

**JavaScript 布尔对象:**
JavaScript 中的布尔对象是布尔值的对象包装器。JavaScript 中的布尔值也可以使用 new 关键字来定义。
**语法:**

```
new Boolean(value)
```

**代码#3:**

## java 描述语言

```
<!DOCTYPE html>
<html>

<body>
    <script>
        var v1 = false;
        var v2 = new Boolean(false);
        var v3 = new Boolean("");
        var v4 = new Boolean(0);
        var v5 = new Boolean(true);
        var v6 = new Boolean("GeeksforGeeks");
        document.write('v1 = ' + v1);
        document.write("<br>");
        document.write('v2 = ' + v2);
        document.write("<br>");
        document.write('v3 = ' + v3);
        document.write("<br>");
        document.write('v4 = ' + v4);
        document.write("<br>");
        document.write('v5 = ' + v5);
        document.write("<br>");
        document.write('v6 = ' + v6);
    </script>
</body>
</html>
```

**输出:**

```
v1 = false
v2 = false
v3 = false
v4 = false
v5 = true
v6 = true
```

**代码#4:**

## java 描述语言

```
<!DOCTYPE html>
<html>

<body>
    <script>
        var v1 = true;
        var v2 = new Boolean(true);

        document.write('v1 = = v2 is ' + (v1 == v2));
        document.write("<br>");
        document.write('v1 = = = v2 is ' + (v1 === v2));
    </script>
</body>
</html>
```

**输出:**

```
v1 = = v2 is true
v1 = = = v2 is false
```

**注:** *v1 = = = v2* 不成立，因为 v1 和 v2(对象)的类型不一样。
**支持的浏览器:**

*   谷歌 Chrome 6 及以上版本
*   边缘 12 及以上
*   Firefox 4 及以上版本
*   Internet Explorer 9 及以上版本
*   歌剧 12 及以上
*   Safari 5.1 及以上版本