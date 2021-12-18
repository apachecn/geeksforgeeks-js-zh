# JavaScript 布尔原型构造器

> 原文:[https://www . geesforgeks . org/JavaScript-boolean-prototype-constructor/](https://www.geeksforgeeks.org/javascript-boolean-prototype-constructor/)

下面是**布尔原型构造函数**属性的例子。

*   **例:**

    ```
    <script>
            Boolean.prototype.color = function(pro) 
            {
                if (pro == true) {
                    return "Green";
                } else {
                    return "Orange";
                }
            };

            // Creating a new boolean object
            var Obj = new Boolean(true);

            document.write("Color of Gfg = "
                    + Obj.color(true));
    </script>                    
    ```

*   **输出:**

    ```
    Color of Gfg = Green
    ```

**布尔原型构造器**属性用于向所有布尔实例添加新的属性和方法。在创建属性时，所有布尔值都将被赋予该属性，并被赋值，这是默认的，但是在方法的情况下，所有布尔值都可以使用该方法。

**语法:**

```
Boolean.prototype.name = value
```

这里，“名称”指定要使用的属性或方法名称，“值”指定函数使用的值。
**一些与布尔原型属性相关的方法:**

*   **[boolean . prototype . value of():](https://www.geeksforgeeks.org/javascript-boolean-valueof-function/)**它只是返回布尔对象的值。
*   **[Boolean . prototype . tostring():](https://www.geeksforgeeks.org/javascript-boolean-tostring-function/)**这个方法根据布尔值返回一个字符串。

以上构造函数的更多示例代码如下:
**程序 1:**

```
<script>
        function check(v1) {
            if (v1 == true)
                return (v1 + " is True.");
            else
                return (v1 + " is False.");
        }

        // Adding a new property
        Boolean.prototype.myVar = false;

        // Adding a new method
        Boolean.prototype.myMethod = check;

        // Creating a new boolean object
        var Obj1 = new Boolean();

        document.write(Obj1.myMethod(1) + "<br>");
        document.write(Obj1.myMethod(0) + "<br>");
        document.write("myVar = " + Obj1.myVar);

</script>
```

**输出:**

```
1 is True.
0 is False.
myVar = false
```

**程序 2:**

```
<script>
        Boolean.prototype.CheckGeek = function(pro) {
            if (pro == true) {
                return "Pro Geek";
            } else {
                return "Geek";
            }
        };

        // Creating a new boolean object
        var Obj = new Boolean(true);

        document.write("Obj.CheckGeek(true) = " 
                          + Obj.CheckGeek(true) + "<br>");
        document.write("Obj.CheckGeek(false) = " 
                         + Obj.CheckGeek(false) + "<br>");
        document.write("Obj.valueOf() = " 
                                + Obj.valueOf() + "<br>");
        document.write("Obj.toString() = " 
                                        + Obj.toString());

</script>            
```

**输出:**

```
Obj.CheckGeek(true) = Pro Geek
Obj.CheckGeek(false) = Geek
Obj.valueOf() = true
Obj.toString() = true
```

**支持的浏览器:****JavaScript 布尔原型构造器**支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   Mozilla Firefox
*   旅行队
*   歌剧