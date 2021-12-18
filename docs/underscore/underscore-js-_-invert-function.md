# 下划线. js _。反转()功能

> 原文:[https://www . geesforgeks . org/下划线-js-_-反转-函数/](https://www.geeksforgeeks.org/underscore-js-_-invert-function/)

**_。invert()函数**用于返回一个对象的副本，其中对象键转换为值，对象值转换为键。这意味着对象的[键，值]是反向的。

**语法:**

```
_.invert( object )
```

**参数:**该功能接受如上所述的单个参数，描述如下:

*   **对象:**包含保存键值对元素的对象元素。

**返回值:**按照相反的[值，键]顺序返回对象的[键，值]。

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript" 
            src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        var obj = {
            Company: "GeeksforGeeks",
            Address: "Noida",
            Contact: "+91 9876543210",
            Email: "abc@gfg.com"
        }
        console.log(_.invert(obj));
    </script>
</body>

</html>
```

**输出:**
![](img/06ea95b6a9d38329679a88ba76d346c9.png)

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript" 
            src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        var inv = _.invert({
            num1: 10,
            num2: 20,
            num3: 30,
            num4: 40
        });

        console.log(inv);
    </script>
</body>

</html>
```

**输出:**
![](img/f02f48b7588e8e24e5f4770b13ec65a6.png)