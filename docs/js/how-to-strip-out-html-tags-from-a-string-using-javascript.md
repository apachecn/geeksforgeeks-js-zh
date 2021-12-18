# 如何用 JavaScript 从字符串中剥离 HTML 标签？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 从字符串中剥离 html 标记/](https://www.geeksforgeeks.org/how-to-strip-out-html-tags-from-a-string-using-javascript/)

要从字符串中去掉所有的 HTML 标签，JavaScript 中有很多过程。为了剥离标签，我们可以使用 **[替换()功能](https://www.geeksforgeeks.org/javascript-string-replace/)** ，也可以使用 **[。textContent 属性](https://www.geeksforgeeks.org/html-dom-textcontent-property/)** 、 **[。来自 HTML DOM 的 innerText 属性](https://www.geeksforgeeks.org/html-dom-innertext-property/)** 。HTML 标签有两种类型**开始标签**和**结束标签**。

*   **开始标记:**以“ **<** ”开头，后跟 HTML 关键字，以“ **>** ”结尾。< html >、< br >、< title >都是 html 开头标签的一些例子。
*   **结束标记:**以“ **< /** ”开头，后跟 HTML 关键字，以“ **>** ”结尾。< /html >、< /title >都是 html 结束标签的例子。

下面的例子说明了这两种方法:

**示例 1:** 可以使用“<”、“< /”、“>”将单词识别为字符串中的 HTML 标记。以下示例显示了如何使用 **replace()函数**和**正则表达式**去除 HTML 标记，该表达式用于识别输入字符串中的 HTML 标记。正则表达式是找到 HTML 标记并轻松移除它们的更好方法。

*   **程序:**在 JavaScript 中，下面的代码剥离了一串 HTML 标签。

    ```
    <script>
    function removeTags(str) {
        if ((str===null) || (str===''))
            return false;
        else
            str = str.toString();

        // Regular expression to identify HTML tags in 
        // the input string. Replacing the identified 
        // HTML tag with a null string.
        return str.replace( /(<([^>]+)>)/ig, '');
    }
    document.write(removeTags(
        '<html>Welcome to GeeksforGeeks.</html>'));;
    </script>                    
    ```

*   **输出:**

    ```
    Welcome to GeeksforGeeks.
    ```

**例 2:****。textContent 属性**返回指定节点及其所有后代的文本内容。**。innerText 属性**做和**一样的事情。文本内容属性**。

*   **程序:**在 JavaScript 中，下面的代码剥离了一串 HTML 标签。

    ```
    <script>

        // HTML tags contain text
        var html = "<p>A Computer Science "
                 + "Portal for Geeks</p>";
        var div = document.createElement("div");
        div.innerHTML = html;
        var text = div.textContent || div.innerText || "";
        document.write(text)
    </script>
    ```

*   **输出:**

    ```
    A Computer Science Portal for Geeks
    ```