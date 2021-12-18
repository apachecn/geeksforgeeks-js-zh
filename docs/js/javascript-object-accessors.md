# JavaScript |对象访问器

> 原文:[https://www.geeksforgeeks.org/javascript-object-accessors/](https://www.geeksforgeeks.org/javascript-object-accessors/)

有两个定义访问器函数的关键字:全名属性的 getter 和 setter。当访问属性时，使用 getter 的返回值。当一个值被设置时，setter 被调用并传递被设置的值。

**JavaScript Getter(get 关键字):**

**示例:**本示例描述了使用 lang()属性获取语言属性的值。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript Getter 
    </title>
</head>

<body style="text-align:center;">

    <div style="background-color: green;">

        <h1>
            Welcome to GeeksforGeeks!.
        </h1>

        <h2>
            JavaScript Getters
        </h2>

        <p id="GFG"></p>
    </div>

    <script>

        // Create an object:
        var person = {
            name: "geeksforgeeks",
            get lang() {
                return this.name;
            }
        };

        // Display data from the object using a getter
        document.getElementById("GFG").innerHTML
                = person.name;
    </script>
</body>

</html>                    
```

**输出:**
![](img/5e55cf290aa232c578c66cb202d2378a.png)

**JavaScript Setter(set 关键字):**
**示例:**本示例描述了使用 lang()属性设置语言属性的值。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript Getter 
    </title>
</head>

<body style="text-align:center;">

    <div style="background-color: green;">

        <h1>
            Welcome to GeeksforGeeks!.
        </h1>

        <h2>
            JavaScript Getters
        </h2>

        <p id="GFG"></p>
    </div>

    <script>

        // Create an object:
        var person = {
            name: "geeksforgeeks",

            set lang(value) {
                return this.name;
            }
        };

        // Display data from the object using a getter
        document.getElementById("GFG").innerHTML
                = person.name;
    </script>
</body>

</html>                    
```

**输出:**
![](img/745328466b23b5a05e89dde87eeb7e36.png)

**注意:**Internet Explorer 8 不支持 Getters 和 Setters。

**使用吸气剂和沉降剂的原因:**

*   属性和方法的语法是相同的。
*   用来做幕后的事情。
*   他们可以保证更好的数据质量。
*   这个的语法更简单。

**数据质量:**获取器和设置器用于确保更好的数据质量。

在下面给出的示例中，使用 lang 属性，返回语言的小写值。
**示例:**该示例使用 lang 属性，并返回语言的小写值。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Data Quality
    </title>
</head>

<body style="text-align:center;">

    <div style="background-color: green;">

        <h1>Geeksforgeeks !!</h1>

        <b>
            Data Quality : lower case 
            value is returned
        </b>

        <p id="GFG"></p>
    </div>

    <script>
        var person = {
            language : "Geeksforgeeks",

            get lang() {
                return this.language.toLowerCase();
            }
        };

        // Display data from the object using a getter
        document.getElementById("GFG").innerHTML 
                = person.lang;
    </script>
</body>

</html>                    
```

**输出:**
![](img/18e9f1ca989322f28bba25a481d4b0ce.png)