# 如何使用 JavaScript 从字符串中修剪文件扩展名？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 从字符串中修剪文件扩展名/](https://www.geeksforgeeks.org/how-to-trim-a-file-extension-from-string-using-javascript/)

给定一个字符串格式的文件名，任务是使用 JavaScript 从字符串中删除文件扩展名。

*   **replace() method:** This method searches a string for a defined value or a regular expression, and returns a new string with the replaced defined value.

    **语法:**

    ```
    string.replace(searchVal, newvalue)
    ```

    **参数:**

    *   **searchVal:** 必选参数。它指定将被新值替换的值或正则表达式。
    *   **新值:**必选参数。它指定要用搜索值替换的值。

    **返回值:**它返回一个新字符串，其中定义的值已被新值替换。

*   **split() method:** This method is used to split a string into an array of substrings and returns the new array.

    **语法:**

    ```
    string.split(separator, limit)
    ```

    **参数:**

    *   **分隔符:**为可选参数。它指定用于拆分字符串的字符或正则表达式。如果不使用，将返回整个字符串(只有一项的数组)。
    *   **极限:**为可选参数。它指定整数，该整数指定超出拆分限制的拆分项目数将从数组中排除。

    **返回值:**返回一个新数组，包含拆分后的项目。

*   **JavaScript String slice() method:** This method gets parts of a string and returns the extracted parts in a new string. Start and end parameters are used to specify the part of the string to extract. The first character starts from position 0, the second has position 1, and so on.

    **语法:**

    ```
    string.slice(start, end)

    ```

    **参数:**

    *   **启动:**为必输参数。它指定开始提取的位置。第一个字符从位置 0 开始。
    *   **结束:**为可选参数。它指定停止提取的位置(不包括它)。如果不使用，slice()将选择从开始位置到结束位置的所有字符。

    **返回值:**返回一个字符串，代表字符串的提取部分。

*   **JavaScript Array join() Method:** This method adds the elements of an array into a string, and returns the string. The elements will be separated by a passed separator. The default separator is comma (, ).

    **语法:**

    ```
    array.join(separator)

    ```

    **参数:**该方法接受单参数**分隔符**，可选。它指定要使用的分隔符。如果不使用，元素用逗号分隔

    **返回值:**返回一个字符串，表示数组值，用定义的分隔符分隔。

**示例 1:** 本示例使用 **split()、slice()和 join()方法**获取文件名。

```
<!DOCTYPE HTML> 
<html> 
    <head> 
        <title> 
            Trim a file extension from a
            string using JavaScript
        </title>
    </head> 

    <body style = "text-align:center;"> 

        <h1 style = "color:green;" > 
            GeeksForGeeks 
        </h1>

        <p id = "GFG_UP" style = 
            "font-size: 15px; font-weight: bold;">
        </p>

        <button onclick = "gfg_Run()"> 
            click here
        </button>

        <p id = "GFG_DOWN" style = 
            "color:green; font-size: 20px; font-weight: bold;">
        </p>

        <script>
            var el_up = document.getElementById("GFG_UP");
            var el_down = document.getElementById("GFG_DOWN");
            var fName = "fileName.jpg";
            el_up.innerHTML = "String = '"+fName + "'";

            function gfg_Run() {
                el_down.innerHTML = fName.split('.').slice(0, -1).join('.');
            }         
        </script> 
    </body> 
</html>                    
```

**输出:**

*   **点击按钮前:**
    ![](img/22d86cb8996c2f770a9aa5c48309a371.png)
*   **点击按钮后:**
    ![](img/0a2494f5810c3d64e525eb06785df10a.png)

**示例 2:** 本示例通过使用**正则表达式**和**替换()方法**来获取文件名。

```
<!DOCTYPE HTML> 
<html> 
    <head> 
        <title>
            Trim a file extension from a
            string using JavaScript
        </title>
    </head> 

    <body style = "text-align:center;"> 

        <h1 style = "color:green;" > 
            GeeksForGeeks 
        </h1>

        <p id = "GFG_UP" style = 
            "font-size: 15px; font-weight: bold;">
        </p>

        <button onclick = "gfg_Run()"> 
            click here
        </button>

        <p id = "GFG_DOWN" style =
            "color:green; font-size: 20px; font-weight: bold;">
        </p>

        <script>
            var el_up = document.getElementById("GFG_UP");
            var el_down = document.getElementById("GFG_DOWN");
            var fName = "fileName.jpg";
            el_up.innerHTML = "String = '" + fName + "'";

            function gfg_Run() {
                el_down.innerHTML =fName.replace(/\.[^/.]+$/, "")
            }         
        </script> 
    </body> 
</html>                    
```

**输出:**

*   **点击按钮前:**
    ![](img/22d86cb8996c2f770a9aa5c48309a371.png)
*   **点击按钮后:**
    ![](img/0a2494f5810c3d64e525eb06785df10a.png)