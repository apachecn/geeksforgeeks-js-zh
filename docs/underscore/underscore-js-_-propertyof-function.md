# 下划线. js | _。()功能属性

> 原文:[https://www . geesforgeks . org/下划线-js-_-propertyof-function/](https://www.geeksforgeeks.org/underscore-js-_-propertyof-function/)

**_。propertyOf()函数**是 _ 的逆函数。property()函数。此函数将对象作为参数，并返回一个函数，该函数将返回所提供属性的值。

**语法:**

```
_.propertyOf( object )
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **对象:**该参数保存函数需要返回的对象的值。

**返回值:**返回对象的属性。

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        var info = {
            Company: 'GeeksforGeeks',
            Address: 'Noida',
            Contact: '+91 9876543210'
        };

        console.log(_.propertyOf(info)('Company'));
    </script>
</body>

</html>
```

**输出:**
![](img/2e817a3dfedaeceaf97dd86973ce1c13.png)

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        var info = {
            Company: { name: 'GeeksforGeeks' },
            Contact: { Address: 
                { AddressInfo: 'Noida', ContNo: '+91 9876543210' } }
        };

        console.log(_.propertyOf(info)('Company', 'name'));
        console.log(_.propertyOf(info)('Contact', 'Address', 'AddressInfo'));
    </script>
</body>

</html>
```

**输出:**
![](img/9afbb92c98aa9e29fd9de25ef5fddbd5.png)