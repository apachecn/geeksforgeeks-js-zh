# 如何在 JavaScript 中获取关联数组键列表？

> 原文:[https://www . geesforgeks . org/如何获取 javascript 中的关联数组键列表/](https://www.geeksforgeeks.org/how-to-get-a-list-of-associative-array-keys-in-javascript/)

**关联数组:**关联数组用于存储键值对。例如，要将学生不同科目的分数存储在数组中，数字索引数组不是最佳选择。相反，我们可以使用各自主题的名称作为关联数组中的键，值将是它们各自获得的分数。在关联数组中，键值对与 **:** 符号相关联。

**方法 1:** 在该方法中，使用 foreach 循环遍历整个关联数组，并显示数组的关键元素。

**语法:**

```
for (var key in dictionary) {
  // do something with key
}
```

**示例:**程序循环通过关联数组和打印键。

```
<script>
    // Script to Print the keys using loop
    // Associative array
    var arr = {
        "Newton": "Gravity",
        "Albert": "Energy",
        "Edison": "Bulb",
        "Tesla": "AC"
    };

document.write("Keys are listed below <br>");

// Loop to print keys
for (var key in arr) {
    if (arr.hasOwnProperty(key)) {

        // Printing Keys
        document.write(key + "<br>");
    }
} 
</script>
```

**输出:**

```
Keys are listed below 
Newton
Albert
Edison
Tesla

```

**方法二:**使用 **[Object.keys()](https://www.geeksforgeeks.org/object-keys-javascript/)** 函数:Object.keys()是 javascript 中的一个内置函数，可以用来获取数组的所有键。

**语法:**

```
Object.keys(obj)

```

**示例:**下面的程序演示了如何使用 Object.keys()来访问关联数组的键。

```
<script>
    // Script to Print the keys 
    // using Object.keys() function
    // Associative array
    var arr = {
        "Newton": "Gravity",
        "Albert": "Energy",
        "Edison": "Bulb",
        "Tesla": "AC"
    };
    // Get the keys
    var keys = Object.keys(arr);

    document.write("Keys are listed below <br>");

    // Printing keys
    document.write(keys);
</script>
```

**输出:**

```
Keys are listed below 
Newton, Albert, Edison, Tesla

```