# JavaScript 转义()函数

> 原文:[https://www.geeksforgeeks.org/javascript-escape-function/](https://www.geeksforgeeks.org/javascript-escape-function/)

下面是**转义()函数**的例子。

*   **例:**

    ```
    <script>
       // Special character encoded with
       // escape function
       document.write(escape("Geeks for Geeks!!!"));

       document.write("<br>");

       // Print encoded string using escape() function
       // Also include exceptions i.e. @ and .
       document.write(escape("To contribute articles contact"+
                        " us at review-team@geeksforgeeks.org"));
    </script>                    
    ```

*   **输出:**

    ```
    Geeks%20for%20Geeks%21%21%21
    To%20contribute%20articles%20contact%20us%20atcontribute
    @geeksforgeeks.org 
    ```

**escape()函数**将字符串作为参数，并对其进行编码，以便将其传输到支持 ASCII 字符的任何网络中的任何计算机。

**语法:**

```
escape(string)
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **字符串:**该参数保存将要编码的字符串。

**返回值:**这个函数返回一个编码的字符串。

**注意:**该功能只对特殊字符进行编码，该功能不复杂。
T3】例外:@–+。/ * _

上述功能的更多示例代码如下:

**程序 1:**

```
<script>
   // Special character encoded with
   // escape function
   document.write(escape("Geeks for Geeks!!!"));

   document.write("<br>");

   // Print encoded string using escape() function
   // Also include exceptions i.e. @ and .
   document.write(escape("A Computer Science Portal"));
</script>                    
```

**输出:**

```
Geeks%20for%20Geeks%21%21%21
A%20Computer%20Science%20Portal
```

**程序 2:**

```
<script>
    // Special character encoded with
    // escape function
    document.write(escape("GeeksforGeeks"));

    document.write("<br>");

    // Print encoded string using escape() function
    // Also include exceptions i.e. @ and .
    document.write(escape("A#Computer-Science"+
                          "%Portal@for*Geeks"));
</script>                  
```

**输出:**

```
GeeksforGeeks
A%23Computer-Science%25Portal@for*Geeks
```

**支持的浏览器:**

*   谷歌 Chrome 1 及以上版本
*   Internet Explorer 3 及以上版本
*   边缘 12 及以上
*   Mozilla Firefox 1 及以上版本
*   Safari 1 及以上
*   歌剧 3 及以上