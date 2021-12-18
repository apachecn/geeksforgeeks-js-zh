# JavaScript unescape()函数

> 原文:[https://www.geeksforgeeks.org/javascript-unescape/](https://www.geeksforgeeks.org/javascript-unescape/)

**先决条件:** [JavaScript 转义()函数](https://www.geeksforgeeks.org/javascript-escape-function/)

下面是 **unescape()函数**的例子。

*   **例:**

    ```
    <script>
       // Special character encoded with
       // escape function
       document.write(unescape("Geeks%20for%20Geeks%21%21%21"));

       document.write("<br>");

       // Print encoded string using escape() function
       // Also include exceptions i.e. @ and .
       document.write(unescape("To%20contribute%20articles%20contact"+
                       "%20us%20atreview-team@geeksforgeeks.org"));
    </script>                    
    ```

*   **输出:**

    ```
    Geeks for Geeks!!!
    To contribute articles contact us at 
    review-team@geeksforgeeks.org
    ```

JavaScript 中的 **unescape()函数**将一个字符串作为参数，并用于解码由 **escape()函数**编码的字符串。当通过 unescape()解码时，字符串中的十六进制序列被它们所代表的字符替换。

**语法:**

```
unescape(string)
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **string:** This parameters holds the string that will be decoded.

    **返回值:**该函数返回解码后的字符串。

    **注意:**此功能只解码特殊字符，此功能不复杂。
    T3】例外:@–+。/ * _

    以上功能的更多示例代码如下:
    **程序 1:**

    ```
    <script>
       // Special character encoded with
       // escape function
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
                    "at review-team@geeksforgeeks.org")
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

    Encoded : To%20contribute%20articles%20contact%20us%20at%20review-team@geeksforgeeks.org
    Decoded : To contribute articles contact us at review-team@geeksforgeeks.org

    ```

    **支持的浏览器:**

    *   谷歌 Chrome 1 及以上版本
    *   边缘 12 及以上
    *   Internet Explorer 3 及以上版本
    *   Mozilla Firefox 1 及以上版本
    *   Safari 1 及以上
    *   歌剧 3 及以上