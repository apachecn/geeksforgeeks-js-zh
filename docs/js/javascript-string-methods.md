# JavaScript |字符串方法

> 原文:[https://www.geeksforgeeks.org/javascript-string-methods/](https://www.geeksforgeeks.org/javascript-string-methods/)

最初，只为浏览器创建了 JavaScript 语言。但是现在，这种语言也在许多其他环境中使用。它是一种用于创建和控制动态网站内容的脚本语言。这意味着网页可以在用户屏幕上移动、刷新或更改，而无需手动重新加载网页。

**Javascript 中的字符串:**字符串是帮助保存可以表示的数据的文本。

一个 JavaScript 字符串存储一系列像“极客”这样的字符。字符串可以是双引号或单引号内的任何文本。例如，

```
 var gfg= "geeksforgeeks";
```

。

字符串索引从 0 开始。第一个字符位于位置 0，第二个字符位于位置 1，如下所示。我们可以调用 JavaScript 的任何预定义方法，因为它会自动从字符串原语转换为对象。

1.  **charAt(indexOfCharacter) method:** This method returns the character at the specified index. String in JavaScript has zero-based indexing.
    **Parameters:** This method accepts single parameter **indexOfCharacter** that holds the Index of the character of any string.

    **示例:**这个示例描述了 JavaScript 字符串 charAt()方法。

    ```
    <script>
        let gfg = 'GeeksforGeeks';
        let geeks = 'GfG is the best platform to "
            + "learn and experience Computer Science.';

        // Print the string as it is
        document.write(gfg); 
        document.write("<br>");

        document.write(geeks); 
        document.write("<br>");

        // As string index starts from zero
        // It will return first character of string
        document.write(gfg.charAt(0)); 
        document.write("<br>");

        document.write(geeks.charAt(5));
    </script>
    ```

    **输出:**

    ```
    GeeksforGeeks
    GfG is the best platform to learn 
    and experience Computer Science.
    G
    s

    ```

2.  **字符编码(indexOfCharacter)方法:**该方法返回一个数字，该数字代表位于*指定索引*的字符的 **Unicode** 值。此方法接受一个参数。

    **示例:**这个示例描述了 JavaScript String charCodeAt()方法。

    ```
    <script>
        let gfg = 'GeeksforGeeks';
        let geeks = 'GfG is the best platform "
                + "to learn and experience "
                + "Computer Science.';

        // Return a number indicating Unicode
        // value of character at index 0 ('G')
        document.write(gfg.charCodeAt(0));
        document.write("<br" >);
        document.write(geeks.charCodeAt(5));
    </script>
    ```

    **输出:**

    ```
    71
    115

    ```

3.  **concat( objectOfString)方法:**此方法组合两个字符串的文本，并返回一个新的组合或连接的字符串。为了连接两个字符串，我们在一个字符串对象上使用 **concat()** 方法，并发送另一个字符串对象作为参数。此方法接受一个参数。变量包含双引号或单引号中的文本。

    **示例:**本示例描述了 JavaScript String concat()方法。

    ```
    <script>
        let gfg = 'GFG ';
        let geeks = 'stands for GeeksforGeeks';

        // Accessing concat method on an object
        // of String passing another object 
        // as a parameter
        document.write(gfg.concat(geeks));

    </script>
    ```

    **输出:**

    ```
    GFG stands for GeeksforGeeks

    ```

4.  **end with(query string，length)方法:**该方法检查字符串是否以指定的字符串或字符结尾。如果字符串以提供的字符串结尾，则该方法返回“true”，否则返回“false”。此方法区分大小写。此方法接受两个参数。

    *   **查询字符串:**要搜索的字符串。
    *   **长度:**默认值为您提供的字符串长度。

    **示例:**本示例描述了 JavaScript String endsWith()方法。

    ```
    <script>
        let gfg = 'GFG ';
        let geeks = 'stands for GeeksforGeeks';

        // Accessing method of object geeks if
        // 'geeks' ends with 'ks', method 
        // return true
        document.write(geeks.endsWith('ks'));
    </script>
    ```

    **输出:**

    ```
    true

    ```

5.  **fromCharCode(UNICODE_NUMBER)方法:**此方法将 UNICODE 值转换为字符。这是字符串对象的静态方法。第一种方法不是从字符串变量开始。此方法返回给定特定 UNICODE 的字符。该方法接受一个参数 **UNICODE-NUMBER** ，该参数保存您想要字符的数字。

    **示例:**本示例描述了 JavaScript String fromCharCode()方法。

    ```
    <script>
        let gfg = 'GFG ';
        let geeks = 'stands for GeeksforGeeks';

        // Given a number as argument
        // Output will be 'E' as 69 stands for 'E'
        document.write(String.fromCharCode(69));

        // Output will be 'a' as 97 stands for 'a'
        document.write(String.fromCharCode(97));
    </script>
    ```

    **输出:**

    ```
    Ea

    ```

6.  **包含(queryString)方法:**该方法检查字符串变量是否包含特定字符串。如果字符串存在于变量字符串变量中，此方法返回“真”，否则返回“假”。此方法区分大小写。该方法接受单个参数**查询字符串**，该参数包含您想要检查其是否存在的字符串。

    **示例:**本示例描述了 JavaScript String includes()方法。

    ```
    <script>
    let gfg = 'GFG ';
    let geeks = 'stands for GeeksforGeeks';

    // 'GFG' is present in gfg variable
    // returns "true"
    document.write(gfg.includes('GFG'));
    document.write("<br>");

    // It is case-sensitive
    // returns "false"
    document.write(gfg.includes('gfg'));
    </script>
    ```

    **输出:**

    ```
    true
    false

    ```

7.  **indexOf(queryString)方法:**该方法返回给定查询字符串第一次出现的索引。如果字符串变量中不存在给定的字符或字符串，则此方法返回-1。此方法区分大小写。该方法接受保存字符或字符串的单参数**查询字符串**，以获取该字符串的索引。

    **示例:**本示例描述了 JavaScript String indexOf()方法。

    ```
    <script>
    let gfg = 'GFG ';
    let geeks = 'stands for GeeksforGeeks';

    // 'G' is present at 0 index.
    document.write(gfg.indexOf('G')); 
    document.write("<br>");

    // 'GFa' is not in gfg variable
    // returns -1
    document.write(gfg.indexOf('GFa'));
    document.write("<br>");

    // Space is present at 3rd index
    document.write(gfg.indexOf(' '));
    </script>
    ```

    **输出:**

    ```
     0
    -1
     3

    ```

8.  **repeat(number)方法:**此方法返回一个字符串，该字符串具有现有字符串的副本数。此方法接受单个参数**编号**，该参数保存现有字符串所需的副本数量。

    **示例:**本示例描述了 JavaScript String repeat()方法。

    ```
    <script>
    let gfg = 'GFG ';
    let geeks = 'stands for GeeksforGeeks';

    // Return 3 copies of String 
    // present in variable gfg
    document.write(gfg.repeat(3));
    </script>
    ```

    **输出:**

    ```
    GFG GFG GFG

    ```

9.  **replace(replaceValue，replaceWithValue)方法:**此方法返回带有更改的字符串。此方法区分大小写。
    该方法接受两个参数，如上所述，如下所述:

    *   **替换值:**此参数保存您要替换的字符。
    *   **replaceWithValue:** 此参数保存要替换的字符。

    **示例:**本示例描述了 JavaScript String replace()方法。

    ```
    <script>
    let gfg = 'GFG ';
    let geeks = 'stands for GeeksforGeeks';

    // Replace 'FG' in gfg with
    //'fg'
    document.write(gfg.replace('FG', 'fg'));
    </script>
    ```

    **输出:**

    ```
    Gfg

    ```

10.  **搜索(queryString)方法:**该方法搜索指定的值或正则表达式。如果找到匹配项，此方法返回匹配项的位置，如果没有找到，则返回-1。此方法区分大小写。该方法接受单个参数**查询字符串**，该参数保存您想要获取位置的字符串。

    **示例:**本示例描述了 JavaScript String search()方法。

    ```
    <script>
    let gfg = 'GFG ';
    let geeks = 'stands for GeeksforGeeks';

    // 'for' is not present in gfg
    // returns -1
    document.write(gfg.search('for'));
    document.write("<br>");

    //'for' is present in geeks
    // return the index from where it starts
    console.log(geeks.search('for'));
    </script>
    ```

    **输出:**

    ```
    -1
    7

    ```

11.  **切片(startIndex，endIndex)方法:**该方法提取字符串的一部分并返回一个新的字符串。

    此方法接受两个参数。

    *   **开始索引:**此参数保存您想要提取的索引。包括在内。
    *   **endIndex:** 此参数保存索引，直到您想要提取的位置。它被排除在外。

    **示例:**本示例描述了 JavaScript String slice()方法。

    ```
    <script>
    let gfg = 'GFG ';
    let geeks = 'stands for GeeksforGeeks';

    // Starts from 2nd index
    // ends at 7th index
    document.write(geeks.slice(2, 8));

    </script>
    ```

    **输出:**

    ```
    ands f

    ```

12.  **split(character) Method:** This method splits the string into an array of sub-strings. This method returns an array. This method accepts single parameter **character** on which you want to split the string.

    **示例:**本示例描述了 JavaScript String split()方法。

    ```
    <script>
    let gfg = 'GFG '
    let geeks = 'stands-for-GeeksforGeeks'

    // Split string on '-'. 
    console.log(geeks.split('-'))

    </script>
    ```

    **输出:**

    ```
    stands,for,GeeksforGeeks

    ```

13.  **start with(query string)方法:**该方法检查字符串是否以给定的查询字符串开头。如果字符串以提供的查询字符串开头，则该方法返回“true”，否则返回“false”。此方法接受单个参数**查询字符串**，您想检查现有字符串是否以它开头。

    **示例:**本示例描述了 JavaScript String startsWith()方法。

    ```
    <script>
    let gfg = 'GFG ';
    let geeks = 'stands-for-GeeksforGeeks';

    // String stored in geeks
    // starts with 'stand'
    // Returns "true"
    document.write(geeks.startsWith('stand'));

    </script>
    ```

    **输出:**

    ```
    true

    ```

14.  **toLowerCase(stringVariable)方法:**该方法将字符串中存在的所有字符转换为小写，并返回一个包含所有小写字符的新字符串。此方法接受单参数**字符串变量**字符串，您想要转换为小写。

    **示例:**这个示例描述了 JavaScript String toLowerCase()方法。

    ```
    <script>
    let gfg = 'GFG ';
    let geeks = 'stands-for-GeeksforGeeks';

    document.write(geeks.toLowerCase(geeks));

    </script>
    ```

    **输出:**

    ```
    stands-for-geeksforgeeks

    ```

15.  **toUpperCase(stringVariable) Method:** This method converts all the character present in String to upper case and returns a new String with all character in upper case. This method accepts single parameter **stringVariable** string that you want to convert in upper case.

    **示例:**本示例描述了 JavaScript String toUpperCase()方法。

    ```
    <script>
    let gfg = 'GFG '
    let geeks = 'stands-for-GeeksforGeeks';

    document.write(geeks.toUpperCase(geeks)) ; 
    </script>
    ```

    **输出:**

    ```
    STANDS-FOR-GEEKSFORGEEKS

    ```

16.  **trim() Method:** This method is used to remove either white spaces from the given string. This method returns a new string with removed white spaces. This method called on a String object. This method doesn’t accept any parameter.

    **示例:**本示例描述了 JavaScript String trim()方法。

    ```
    <script>
    let gfg = 'GFG    ';
    let geeks = 'stands-for-GeeksforGeeks';

    // Storing new object of string
    // with removed white spaces
    var newGfg = gfg.trim();

    // Old length
    document.write(gfg.length);
    document.write("<br>");

    // New length
    document.write(newGfg.length)
    </script>
    ```

    **输出:**

    ```
    7
    3

    ```