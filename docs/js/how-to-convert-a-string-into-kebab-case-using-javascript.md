# 如何用 JavaScript 将一个字符串转换成烤串案例？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 将字符串转换为烤肉串/](https://www.geeksforgeeks.org/how-to-convert-a-string-into-kebab-case-using-javascript/)

给定一个带有空格、驼色或蛇纹字母的字符串，任务是找到下面字符串的烤串。

**例如:**

```
Input:  Geeks For Geeks
Output: geeks-for-geeks

Input:   GeeksForGeeks
Output:  geeks-for-geeks

Input:  Geeks_for_geeks
Output: geeks-for-geeks
```

这可以通过以下方式实现:

**方法 1:使用替换方法**

这里我们有一个名为 kebabCase 的函数，它接受一个字符串，并在转换 kebabCase 案例后返回一个字符串。这里我们使用 replace 方法两次，因为第一个 replace 方法是获取所有接近大写字母的字母，并用连字符替换它们。第二个替换函数用于获取空格和下划线，并用连字符替换它们。

## java 描述语言

```
<script>
    const kebabCase = string => string
        .replace(/([a-z])([A-Z])/g, "$1-$2")
        .replace(/[\s_]+/g, '-')
        .toLowerCase();

    console.log(kebabCase('Geeks For Geeks'));
    console.log(kebabCase('GeeksForGeeks'));
    console.log(kebabCase('Geeks_For_Geeks'));
</script>
```

**输出:**

```
geeks-for-geeks
geeks-for-geeks
geeks-for-geeks
```

**方法 2:使用匹配方法**

这里，我们使用检查空格、大写字母和下划线的 map 方法。它创建一个数组，并推送分隔字符串的单词。现在使用连字符 ***连接()连接数组。*** 之后将整个字符串转换成小写。

## java 描述语言

```
<script>
    const kebabCase = str => str
        .match(/[A-Z]{2,}(?=[A-Z][a-z]+[0-9]*|\b)|[A-Z]?[a-z]+[0-9]*|[A-Z]|[0-9]+/g)
        .join('-')
        .toLowerCase();

    console.log(kebabCase('Geeks For Geeks'));
    console.log(kebabCase('GeeksForGeeks'));
    console.log(kebabCase('Geeks_For_Geeks'));
</script>
```

**输出:**

```
geeks-for-geeks
geeks-for-geeks
geeks-for-geeks
```