# 下划线 _。toPath()功能

> 原文:[https://www.geeksforgeeks.org/underscore-_-topath-function/](https://www.geeksforgeeks.org/underscore-_-topath-function/)

下划线。toPath()函数用于将给定值转换为属性路径数组。
**语法:**

```
_.toPath('key')
```

**参数:**该方法接受如上所述的单个参数，如下所述。

**键:**需要转换为路径数组的键值。

**返回值:**新属性路径数组。

下面的例子说明了 _。getPath()函数是下划线

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdn.jsdelivr.net/npm/underscore@latest/underscore-umd-min.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        // Use of _.toPath() method 
        let gfg = _.toPath(['geeks', 'for', 'geeks']);

        // Printing the output  
        console.log(gfg);
    </script>
</body>

</html>
```

**输出:**

```
["geeks","for","geeks"]

```

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdn.jsdelivr.net/npm/underscore@latest/underscore-umd-min.js">
    </script>
</head>

<body>
    <script type="text/javascript">
        var originalToPath = _.toPath;
        _.mixin({
            toPath: function (path) {
                return _.isString(path) ? 
                    path.split('.') : originalToPath(path);
            }
        });
        console.log({
            a: [{
                b: 5
            }]
        }, 'a.0.b');
    </script>
</body>

</html>
```

**输出:**

```
{"a":[{"b":5}]}
 a.0.b
```

**参考:**T2】https://underscorejs.org/#toPath