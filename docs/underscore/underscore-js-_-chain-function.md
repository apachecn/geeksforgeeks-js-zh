# 下划线. js _。链条()功能

> 原文:[https://www . geesforgeks . org/下划线-js-_-链-函数/](https://www.geeksforgeeks.org/underscore-js-_-chain-function/)

**下划线. js** 是一个 JavaScript 库，它提供了许多有用的函数，这些函数在很大程度上有助于编程，比如映射、过滤、调用等，甚至不使用任何内置对象。

**_。chain()函数**是 JavaScript 的下划线. js 库中的一个内置函数，用来查找一个包装好的对象。此外，调用此*对象*上的方法将继续返回包装的对象，直到调用*值*。

**语法:**

```
_.chain(obj)
```

**参数:**接受单个参数，具体如下:

*   **obj:** 是陈述的对象。

**返回值:**这个方法返回一个包装好的对象。

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
    </script>
</head>

<body>
    <script>
        console.log(_.chain([99, 3, 4, 6]).push(100));
    </script>
</body>

</html>
```

**输出:**

```
[99, 3, 4, 6, 100]
```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
    </script>
</head>

<body>
    <script>
        var author_article = [
            { author: 'Nidhi1352', articles: 792 },
            { author: 'Nisha95', articles: 590 },
            { author: 'Rohit01', articles: 450 }
        ];

        var experienced = _.chain(author_article)
            .sortBy(function (author_article) 
                { return author_article.article; })
            .map(function (author_article) {
                return author_article.author +
                    ' wrote ' + author_article.articles 
                    + ' articles! ';
            })
            .first()
            .value();
        console.log(experienced);
    </script>
</body>

</html>
```

**输出:**

```
Nidhi1352 wrote 792 articles!
```

**参考:**T2】https://underscorejs.org/#chain