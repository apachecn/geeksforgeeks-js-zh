# 如何检查 JavaScript 中字符串是否只包含数字？

> 原文:[https://www . geesforgeks . org/如何检查字符串是否只包含 javascript 中的数字/](https://www.geeksforgeeks.org/how-to-check-if-string-contains-only-digits-in-javascript/)

给定一个字符串，任务是检查它是否只包含数字。

**JavaScript test()方法:**该方法测试字符串中的模式。如果找到匹配项，此方法返回 true，否则返回 false。

**语法:**

```
RegExpObject.test(str)
```

**参数:**该功能接受单参数**字符串**，这是必需的。它指定要搜索的字符串。

**示例 1:** 本示例使用**正则表达式**检查非数字字符串。

```
<!DOCTYPE HTML> 
<html> 
    <head> 
        <title> 
            Check if string contains only digits
        </title>
    </head> 

    <body style = "text-align:center;" id = "body"> 

        <h1 style = "color:green;" > 
            GeeksForGeeks 
        </h1>

        <p id = "GFG_UP" style = "font-size: 15px; font-weight: bold;">
        </p>

        <button onclick = "gfg_Run()"> 
            check
        </button>

        <p id = "GFG_DOWN" style = 
            "color:green; font-size: 20px; font-weight: bold;">
        </p>

        <script>
            var el_up = document.getElementById("GFG_UP");
            var el_down = document.getElementById("GFG_DOWN");
            var path = "4323424242";
            el_up.innerHTML = "String = '"+path + "'";

            function gfg_Run() {
                el_down.innerHTML = /^\d+$/.test(path);
            }         
        </script> 
    </body> 
</html>                    
```

**输出:**

*   **点击按钮前:**
    ![](img/d3363f96ee65b3f0c9d289e14b77a694.png)
*   **点击按钮后:**
    ![](img/9eda724411f284ed67206f6b8224d8bb.png)

**示例 2:** 本示例使用**正则表达式**检查非数字字符串。

```
<!DOCTYPE HTML> 
<html> 
    <head> 
        <title> 
            Check if string contains only digits
        </title>
    </head> 

    <body style = "text-align:center;" id = "body"> 

        <h1 style = "color:green;" > 
            GeeksForGeeks 
        </h1>

        <p id = "GFG_UP" style = "font-size: 15px; font-weight: bold;">
        </p>

        <button onclick = "gfg_Run()"> 
            check
        </button>

        <p id = "GFG_DOWN" style = 
            "color:green; font-size: 20px; font-weight: bold;">
        </p>

        <script>
            var el_up = document.getElementById("GFG_UP");
            var el_down = document.getElementById("GFG_DOWN");
            var path = "+4323424242";
            el_up.innerHTML = "String = '"+path + "'";

            function gfg_Run() {
                el_down.innerHTML = !/\D/.test(path);
            }         
        </script> 
    </body> 
</html>                    
```

**输出:**

*   **点击按钮前:**
    ![](img/5e1402f3d68c2c53b9f4a24030ed4f64.png)
*   **点击按钮后:**
    ![](img/80e3268d12fa9a4df6353bf2dbcc49d3.png)