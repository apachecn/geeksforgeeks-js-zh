# JavaScript |类

> 原文:[https://www.geeksforgeeks.org/javascript-classes/](https://www.geeksforgeeks.org/javascript-classes/)

新版 [JavaScript (ES6)的引入引入了类](https://www.geeksforgeeks.org/es6-classes/)的使用，而不是函数。类类似于函数。他们用 class 关键字代替 function 关键字。
他们用构造函数方法初始化。

**语法:**

```
class classname {
  constructor(parameter) {
    this.classname = parameter;
  }
}
```

下面的例子说明了 JavaScript 类:

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<body>
    <center>
        <h1 style="color: green;">
            GeeksforGeeks
        </h1>

<p>
          A Computer Science Portal for Geeks
        </p>

        <b>JavaScript Classes</b>

        <p id="demo"></p>

        <script>
            class class_name {
                constructor(value) {
                    this.classes = value;
                }
            }

            myvalue = new class_name("GeeksforGeeks");

            document.getElementById("demo").innerHTML =
              myvalue.classes;
        </script>
    </center>
</body>

</html>
```

**输出:**

![](img/3bb20353a8b5cbb27cce81cf64f40b8c.png)