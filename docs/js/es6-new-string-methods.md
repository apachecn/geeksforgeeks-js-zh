# ES6 |新字符串方法

> 原文:[https://www.geeksforgeeks.org/es6-new-string-methods/](https://www.geeksforgeeks.org/es6-new-string-methods/)

在 [ES6](https://www.geeksforgeeks.org/introduction-to-es6/) 中，String 增加了四个新方法。当涉及到在 [JavaScript](https://www.geeksforgeeks.org/javascript-tutorial/) 中的字符串操作时，这些方法对程序员来说就像是一个福音。在日常编程中，我们经常处理字符串。前三种方法还减少了某些任务对正则表达式正则表达式的依赖。下面描述了四种 ES6 新字符串方法:

1.  **[startsWith( queryString, position ) Method](https://www.geeksforgeeks.org/javascript-string-startswith/):** This method returns either **true**, if the string starts with the provided string from the specified position, otherwise **false**. This method is **case-sensitive**. This method accepts two arguments :
    *   **查询字符串:**必须在字符串开头搜索的字符串。
    *   **位置(可选):**开始搜索的位置。请注意，其默认值为 0。

    下面的例子说明了第一种方法 **ES6 新字符串方法**(开始于(查询字符串，位置))。

    **示例:**

    ```
    < script >
    let str = "GeeksforGeeks";

    console.log(str.startsWith("Geeks"));

    // Here specified position is 5, that means
    // searching will start from 'f' whose index
    // in string str is 5
    console.log(str.startsWith("for", 5));

    console.log(str.startsWith("geeks")); 
    < /script>
    ```

    **输出:**

    ```
    true
    true
    false

    ```

2.  **[endsWith( queryString, length ) Method](https://www.geeksforgeeks.org/javascript-string-endswith/):** This method returns either **true**, if the string ends with the provided string for specified length, otherwise **false**. This method is **case-sensitive**. This method accepts two arguments:
    *   **查询字符串:**必须在字符串末尾搜索的字符串。
    *   **长度(可选):**字符串的长度。请注意，它的默认值是字符串长度。

    下面的例子说明了第二种方法 **ES6 新字符串方法** (endsWith(queryString，length))。

    **示例:**

    ```
    <script>
    let str = "GeeksforGeeks";

    console.log(str.endsWith("Geeks"));

    // Here specified length is 8, that means
    // length of str will be considered as 8
    // and rest will be omitted
    console.log(str.endsWith("for", 8));

    console.log(str.endsWith("geeks"));
    </script>
    ```

    **输出:**

    ```
    true
    true
    false

    ```

3.  **[includes( queryString, position ) Method](https://www.geeksforgeeks.org/javascript-string-includes-method/):** This method returns either **true** if the string is present in the provided string, otherwise returns **false**. This method is **case-sensitive**. This method accepts two arguments:
    *   **查询字符串:**字符串中要搜索的字符串。
    *   **位置(可选):**开始搜索的位置。请注意，其默认值为 0。

    下面的例子说明了 **ES6 新字符串方法**的第三种方法(包括(查询字符串，位置))。

    **示例:**

    ```
    <script>
    let str = "GeeksforGeeks";

    console.log(str.includes("eks"));

    // Here search will start from index 8
    // of str
    console.log(str.includes("for", 8));

    console.log(str.includes("geeks"));
    </script>
    ```

    **输出:**

    ```
    true
    false
    false

    ```

4.  **[repeat( count ) Method](https://www.geeksforgeeks.org/javascript-string-repeat/):** This method accepts single argument which is an integer value that represents the number of times the string is to be repeated. This method returns the newly created string with ‘count’ times repeated old string.

    **注意:**提供的参数即**计数**必须是正整数。

    下面的例子说明了 **ES6 新字符串方法**的第四种方法(重复(计数))。

    **示例:**

    ```
    <script>
    let str = "GeeksforGeeks";
    console.log(str.repeat(2));
    let newStr = str.repeat(3);
    console.log(newStr);
    </script>
    ```

    **输出:**

    ```
    GeeksforGeeksGeeksforGeeks
    GeeksforGeeksGeeksforGeeksGeeksforGeeks

    ```

    **模板文字:**这些文字允许嵌入表达式。单引号或双引号不是它的行为，而是它使用了反斜线“`”。模板文字有两种类型。

    *   **Singleline Strings and Template Literals:** The Singleline Strings and Template Literals contains the single line string below example will illustrate this.

        **示例:**

        ```
        <script>
        var a = "Geeks"; 
        var b = "for"; 
        console.log(`We are the ${a+b+a} `)
        </script>
        ```

        **输出:**

        ```
        We are the GeeksforGeeks 
        ```

    *   **Multiline Strings and Template Literals:** This Multiline Strings and Template Literals contains the multi-line string below example will illustrate this.

        **示例:**

        ```
        <script>
        var a = `GeeksforGeeks`; 
        var b = ` A Online 
        Computer Science 
        Portal for Geeks`; 

        console.log(a + b)
        </script>
        ```

        **输出:**

        ```
        GeeksforGeeks A Online 
        Computer Science 
        Portal for Geeks
        ```

**String.raw()方法:**string . raw()方法用于按原样打印反斜杠，它不会将新行带入控制台。

**示例:**

```
<script>
var geeks = String.raw `A Online Computer \nScience Portal for Geeks`

//Printing backslash as string
console.log(geeks)
</script>
```

**输出:**

```
A Online Computer \nScience Portal for Geek
```

**[String.fromCodePoint()方法:](https://www.geeksforgeeks.org/javascript-string-fromcodepoint/)**String . FromCodePoint()是 JavaScript 中的内置函数，用于返回给定代码点值序列(ASCII 值)的字符串或元素。

**示例:**

```
<script> 

    // Taking some code point values 
    a = String.fromCodePoint(42); 
    b = String.fromCodePoint(66, 65, 102); 

    // Printing the corresponding elements of 
    // the code point value. 
    console.log(a + "<br>") 
    console.log(b) 

</script> 
```

**输出:**

```
*
BAf
```