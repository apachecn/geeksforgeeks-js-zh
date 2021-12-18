# 是 6 |字串

> 原文:[https://www.geeksforgeeks.org/es6-string/](https://www.geeksforgeeks.org/es6-string/)

ES6 JavaScript 中有两种字符串类型**字符串原语**和**字符串对象**。它通过助手方法包装了 JavaScript 的字符串原语。有一些辅助方法。

*   **字符串原语:**当包装类型的方法被调用时，原语自动装箱到其包装类型。它没有助手方法，它只不过是指向原始数据内存引用的指针。所以这里它包装成一个字符串包装器。 **(var i = 1)** 这里它包装成一个整数包装器。
*   **字符串对象:**这是一个字符串对象。字符串对象是在字符串类的帮助下创建的。它用许多辅助方法包装字符串基元数据类型。

**语法:**ES6 JavaScript 中有三个属性提到并描述如下:

```
var stringobject = new String(string);
```

**字符串属性:**

<figure class="table">

| attribute | describe |
| --- | --- |
| Constructor | This property returns a reference to the string function that created the instance prototype. |
| 长度 | This property returns the length of the string. |
| prototype | This property is a global property that can be used by almost all objects. This allows you to add properties and methods to objects, where prototype objects have different behaviors compared with automatic boxing of string primitives. |

</figure>

以下示例说明了这些属性:

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script>
        function hero(id, name) {
            this.id = id;
            this.name = name;
        }

        // Object e
        var e = new hero(123, "GeeksforGeeks");

        // Object e1
        var e1 = new hero(124, "Courses");

        // This prototype property is constant for all objects.
        hero.prototype.group = "Edutech";

        // Returns object reference
        document.write("Constructor Property = " + e.constructor);

        // Returns length
        document.write("<br>Length of emp.name(GeeksforGeeks) = " + e.name.length);

        // Returns the new property(group)
        document.write("<br>Prototype(emp1.name=Courses) group = " + e1.group);

        // Returns the new property(group)
        document.write("<br>Prototype(emp.name=GeeksforGeeks) group = " + e.group);
    </script>
</head>

<body>
</body>

</html>
```

**输出:**

```
Constructor Property = function hero(id, name) { this.id = id; this.name = name; }
Length of emp.name(GeeksforGeeks) = 13
Prototype(emp1.name=Courses) group = Edutech
Prototype(emp.name=GeeksforGeeks) group = Edutech
```

**字符串对象的方法:**这些是字符串对象中可用的方法列表。

<figure class="table">

| way | describe |
| --- | --- |
| 夏拉特(亚的斯亚贝巴) | This method returns the character at the specified index. |
| charCodet(字符) | This method returns the ascii code of the character at the specified index. |
| Concatenation (string) | This method returns the concatenated string. |
| Index (string) | This method returns the starting index of the given string. |
| lastIndexOf(字符串) | This method returns the starting index of the last occurrence of a given string. |
| 【localeCompare(字符串) | This method returns 0, 1 or -1 if the compared strings are equal, and 1 or -1 if the compared strings are not equal, according to the sorting order. |
| 匹配(正则表达式，字符串) | Returns the match of RegExp. |
| 替换(正则表达式，字符串) | Returns the replaced RegExp in the string. |
| 搜索(RegExp) | This method searches for the given word or regex. If a string is passed as a parameter, it will be converted into a regular expression by using a new regular expression (obj). |
| 魏冄(startIndex，endIndex) | This method returns a string from startIndex to endIndex (not included) at the specified index. |
| 子字符串(起始索引，长度) | Returns a string from startIndex to startIndex+length (inclusive) at the specified index. |
| -你好(startIndex，endIndex) | Returns a string from startIndex to endIndex at the specified index (inclusive). |
| Split ("separator", split fraction) | Returns an array split by separators, given b = split fraction, or the whole array if no split is mentioned. |
| to locaallowcase_) | Returns the lowercase string of the current locale. |
| tolocalpearcase() | Returns the uppercase string of the current locale. |
| toLowerCase() | Returns the call string value converted to lowercase. |
| toupperCase() | Returns the character at the specified index. |
| toString() | Returns the call string value converted to uppercase. |
| 的值() | Returns the original value of a String object. |

</figure>

下面的例子将说明这些方法:

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script>
        var str = new String("A Online Computer Science Portal");
        var str1 = new String("Computer Science Portal for Geeks");

        document.write("str.charAt(0) is = " + str.charAt(0));
        document.write("<br>str.charCodeAt(0) is = " + str.charCodeAt(0));

        document.write("<br>");
        document.write("<br>str1.concat('=>Geeks?') = " + str1.concat('=>Geeks?'));

        document.write("<br>");
        document.write("<br>str.indexOf('of') = " + str.indexOf('of'));
        document.write("<br>str.lastIndexOf('of') = " + str.lastIndexOf('of'));

        document.write("<br>");
        document.write("<br>str.localeCompare( 'A Online Computer Science Portal') = "
                       + str.localeCompare('A Online Computer Science Portal'));
        document.write("<br>str.localeCompare( 'Computer Science Portal for Geeks') = "
                       + str.localeCompare('Computer Science Portal for Geeks'));
        document.write("<br>str.localeCompare( 'A Computer Science Portal') = "
                       + str.localeCompare('A Computer Science Portal'));

        document.write("<br>");
        if (str.search("Geeksfor") != -1) {
            document.write("<br>Geeks exist in str.");
        } else {
            document.write("<br>Geeks doesn't exist in str.");
        }

        document.write("<br>");
        document.write("<br>str.slice(5, -1) = " + str.slice(5, -1));
        document.write("<br>str.substr(2, 9) = " + str.substr(2, 9));
        document.write("<br>str.substring(2, 9) = " + str.substring(2, 9));

        document.write("<br>");
        document.write("<br>str.split(' ') = " + JSON.stringify(str.split(' ')));
        document.write("<br>str.split(':', 4) = " + JSON.stringify(str.split(':', 4)));
        document.write("<br>str.split('of', 4) = " + JSON.stringify(str.split('of', 4)));

        document.write("<br>")
        document.write("<br>str1.toLocaleLowerCase( ) = " + str1.toLocaleLowerCase());
        document.write("<br>str1.toLocaleUpperCase() = " + str1.toLocaleUpperCase());
        document.write("<br>str1.toLowerCase( ) = " + str1.toLowerCase());
        document.write("<br>str1.toUpperCase() = " + str1.toUpperCase());

        document.write("<br>")
        document.write("<br>str1.toString() = " + str1.toString());
        document.write("<br>str1.valueOf( ) = " + str1.valueOf());
    </script>
</head>

</html>
```

**输出:**

```
str.charAt(0) is = A
str.charCodeAt(0) is = 65

str1.concat('=>Geeks?') = Computer Science Portal for Geeks=>Geeks?

str.indexOf('of') = -1
str.lastIndexOf('of') = -1

str.localeCompare( 'A Online Computer Science Portal') = 0
str.localeCompare( 'Computer Science Portal for Geeks') = -1
str.localeCompare( 'A Computer Science Portal') = 1

Geeks doesn't exist in str.

str.slice(5, -1) = ine Computer Science Porta
str.substr(2, 9) = Online Co
str.substring(2, 9) = Online

str.split(' ') = ["A","Online","Computer","Science","Portal"]
str.split(':', 4) = ["A Online Computer Science Portal"]
str.split('of', 4) = ["A Online Computer Science Portal"]

str1.toLocaleLowerCase( ) = computer science portal for geeks
str1.toLocaleUpperCase() = COMPUTER SCIENCE PORTAL FOR GEEKS
str1.toLowerCase( ) = computer science portal for geeks
str1.toUpperCase() = COMPUTER SCIENCE PORTAL FOR GEEKS

str1.toString() = Computer Science Portal for Geeks
str1.valueOf( ) = Computer Science Portal for Geeks
```