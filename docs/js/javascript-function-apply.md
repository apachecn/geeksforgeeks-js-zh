# JavaScript |函数应用

> 原文:[https://www.geeksforgeeks.org/javascript-function-apply/](https://www.geeksforgeeks.org/javascript-function-apply/)

apply()方法用于编写可以在不同对象上使用的方法。它不同于函数调用()，因为它将参数作为数组。

**语法:**

```
apply()
```

**返回值:**返回给定函数的方法值。

**示例 1:** 此示例说明了不带参数的 apply()函数。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript apply() Method
        without argument
    </title>
</head>

<body>
    <h1>GeeksforGeeks</h1>

    <h2>
        JavaScript apply() Method
    </h2>

    <h4>
        It displays the details of second student
    </h4>

    <p id="GFG"></p>

    <!-- Script to use apply() method -->
    <script>
        var student = {
            details: function() {
                return this.name + "<br>" + this.class;
            }
        }
        var stud1 = {
            name:"Dinesh",
            class: "11th",
        }
        var stud2 = {
            name:"Vaibhav",
            class: "11th",
        }

        var x = student.details.apply(stud2); 
        document.getElementById("GFG").innerHTML = x; 
    </script>
</body>

</html>                    
```

**输出:**
![](img/98548225a13f94105bd14035c8d222ab.png)

**示例 2:** 本示例用参数说明了 apply()函数。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript apply() Method
        with argument
    </title>
</head>

<body>
    <h1>GeeksforGeeks</h1>

    <h2>
        JavaScript apply() Method
    </h2>

    <h4>
        It displays the details of second student
    </h4>

    <p id="GFG"></p>

    <!-- Script to use apply() method -->
    <script>
        var student = {
            details: function(section, rollnum) {
                return this.name + "<br>" + this.class
                    + " " + section + "<br>" + rollnum;
            }
        }
        var stud1 = {
            name:"Dinesh",
            class: "11th",
        }
        var stud2 = {
            name:"Vaibhav",
            class: "11th",
        }

        var x = student.details.apply(stud2, ["A", "24"]); 
        document.getElementById("GFG").innerHTML = x; 
    </script>
</body>

</html>                    
```

**输出:**
![](img/d7df49436af9015d74effd00bbad4130.png)

**支持的浏览器:**

*   Chrome 1 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 5.5 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上