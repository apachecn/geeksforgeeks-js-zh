# 下划线. js _。查找()功能

> 原文:[https://www . geesforgeks . org/下划线-js-_-find-function/](https://www.geeksforgeeks.org/underscore-js-_-find-function/)

**_。find()函数**查看列表中的每个元素，并返回满足条件的元素的第一个匹配项。如果列表中的任何元素不满足条件，则返回`undefined`值。

**语法:**

```
_.find(list, predicate, [context])
```

**参数:**该函数接受三个参数，如上所述，如下所述:

*   **列表:**此参数用于保存项目列表。
*   **谓词:**此参数用于保存真值条件。
*   **上下文:**需要显示的文本内容。这是一个可选参数。

**返回值:**返回满足条件的元素的第一次出现。

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
        var oddNo = _.find([5, 6, 7, 8, 9, 10],
            function (num) {
                return num % 2 != 0;
            });
        console.log(oddNo); 
    </script>
</body>

</html>
```

**输出:**

```
5
```

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
        var words = ['javascript', 'java', 'unix',
                     'hypertext', 'undescore', 'CSS'];

        const result = words.find(word => word.length == 9);
        console.log(result); 
    </script>
</body>

</html>
```

**输出:**

```
hypertext
```