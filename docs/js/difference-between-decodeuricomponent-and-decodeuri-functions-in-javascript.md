# JavaScript 中 decodeURIComponent()和 decodeURI()函数的区别

> 原文:[https://www . geeksforgeeks . org/decodeuricomponent-and-decodeuri-functions-in-JavaScript/](https://www.geeksforgeeks.org/difference-between-decodeuricomponent-and-decodeuri-functions-in-javascript/)

**decodeURI()** 和 **decodeURIComponent()** 都是用于解码编码的 URI(统一资源标识符)的 Javascript 全局函数。

**decodeURI()函数:**它对以前由 encodeURI()函数编码的字符串进行解码。它通过用它所代表的字符替换每个 **UTF-8** 转义序列来返回一个解码的 URI。

*   **语法:**

    ```
    decodeURI(encodeURI(x));
    ```

*   **参数**它包含单个参数，该参数包含一个先前由 encodeURI()函数编码的字符串，因此结果将再次是 x。
*   **示例:**本示例使用 **decodeURI()** 功能。

    ```
    <!DOCTYPE html>
    <html>

    <head>
        <title>decodeURI() Example</title>
    </head>

    <body>
        <script type="text/javascript">
            var decodeText1 = decodeURI('http://www.testing.com/');
            document.write(decodeText1);
            document.write("<br>");
            var decodeText2 = decodeURI('http%3A%2F%2Fwww.testing.com%2F');
            document.write(decodeText2);
        </script>
    </body>

    </html>
    ```

*   **输出:**

    ```
    http://www.testing.com/
    http%3A%2F%2Fwww.testing.com%2F

    ```

**decodeURIComponent()函数:**它对以前由 encodeURIComponent()函数编码的字符串进行解码。它通过用它所代表的字符替换每个 UTF-8 转义序列来返回解码的 URI 分量。它可以解码%00 到%7F 之间的任何值。

*   **语法:**

    ```
    decodeURIComponent(encodeURIComponent(x));
    ```

*   **参数**单个参数，包含一个先前由 encodeURIComponent()编码的字符串，因此结果将再次为 x。
*   **示例:**该示例位于 decodeURIComponent()

    ```
    <!DOCTYPE html>
    <html>

    <head>
        <title>decodeURIComponent() Example</title>
    </head>

    <body>
        <script type="text/javascript">
            var decodeText1 = decodeURIComponent(
                              'http://www.testing.com/');
            document.write(decodeText1);
            document.write("<br>");
            var decodeText2 = decodeURIComponent(
                      'http%3A%2F%2Fwww.testing.com%2F');
            document.write(decodeText2);
        </script>
    </body>

    </html>
    ```

*   **输出:**

    ```
    http://www.testing.com/
    http://www.testing.com/

    ```

**注意:**两个函数都抛出 **URIError** ，表示字符串中的一个或多个转义序列格式不正确，无法正确解码。

【decodeURIComponent()和 decodeURI()的区别功能:

*   **decodeURI():** 它采用 encodeURI(url)字符串，因此无法解码字符(，/？:@ & = + $ #)*   **decodeURIComponent():** 它需要 encodeURIComponent(url)字符串，以便能够解码这些字符。

    *   **decodeURI():** 它以 encodeURI(url)字符串为参数，返回解码后的字符串。
    *   **decodeURIComponent():** 它以 encodeURIComponent(url)字符串为参数，返回解码后的字符串。
    *   **decodeURI("%41"):** 它返回“A”
    *   **decodeURIComponent(“% 41”)**它返回“A”
    *   **decodeURI(“%26”):**它返回“% 26”
    *   **decodeURIComponent(“% 26”):**它返回“&”