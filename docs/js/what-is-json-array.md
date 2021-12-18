# 什么是 JSON 数组？

> 原文:[https://www.geeksforgeeks.org/what-is-json-array/](https://www.geeksforgeeks.org/what-is-json-array/)

JSON 数组几乎和 [JavaScript 数组](https://www.geeksforgeeks.org/arrays-in-javascript/)一样。JSON 数组可以存储字符串、数组、布尔值、数字、对象或*空值。*在 JSON 数组中，值之间用逗号分隔。可以使用[]运算符访问数组元素。

JSON 数组有不同的类型。让我们借助例子来理解它们。

**JSON 字符串数组:** JSON 字符串数组只包含字符串元素。例如，下面的数组有 6 个字符串元素，“Ram”、“Shyam”、“Radhika”、“阿克谢”、“Prashant”和“Varun”，每个 elemet 用逗号(，)分隔。

```
["Ram", "Shyam", "Radhika", "Akshay", "Prashant", "Varun"]
```

**示例:**这里我们将为 *jsonStringArray* 对象中的键*学生*分配一个 JSON 字符串数组。然后我们使用[ ]运算符访问数组的第一个元素。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<body>
    <p id="para"></p>

    <script>
        var jsonStringArray = {

            // Assigned a JSON array of strings
            // to the key "students".
            "students": ["Ram", "Shyam", "Radhika",
                    "Akshay", "Prashant", "Varun"],
        };

        // It returned an array. Then we accessed
        // the first index of the array
        // (which is "Ram") using [] syntax.
        var x = jsonStringArray.students[0];

        // Set the inner HTML of "para" paragraph 
        // to the value of variable "x". 
        document.getElementById("para").innerHTML = x;
    </script>
</body>

</html>
```

**输出:**

```
Ram
```

**JSON 数字数组:** JSON 数字数组只包含数字元素。例如，下面的数组有 5 个元素，23，44，76，34，98。

```
[23, 44, 76, 34, 98]
```

**示例:**这里我们给*jsonnumberray*对象中的键*标记*分配一个 JSON 数字数组。然后我们使用[ ]运算符访问数组的第一个元素。

## HTML

```
<!DOCTYPE html>
<html>

<body> 
    <p id="para"></p>

    <script>
        var jsonNumberArray = {

            // Assigned a JSON array of numbers
            // to the key "marks".
            "marks": [23, 44, 76, 34, 98],
        };

        // It returned an number array. 
        // Then we accessed the first
        // index of the array
        // (which is 23) using [] syntax.
        var x = jsonNumberArray.marks[0];
        // Set the inner HTML of "para" paragraph 
        // to the value of variable "x". 
        document.getElementById("para").innerHTML = x;
    </script>
</body>

</html>
```

**输出:**

```
23
```

**布尔人的 JSON 数组:**布尔人的 JSON 数组只包含布尔元素(真或假)。例如，下面的数组中有 5 个元素，每个元素要么是真，要么是假。

```
[true, true, true, false, false, true]
```

**示例:**这里我们给*JSON Booleans Array*对象中的键*Booleans*赋值一个 JSON Booleans 数组。然后我们使用[ ]运算符访问数组的第一个元素。

## HTML

```
<!DOCTYPE html>
<html>

<body>
    <p id="para"></p>

    <script>
        var jsonBooleanArray = {

            // Assigned a JSON array of boolean
            // to the key "booleans".
            "booleans": [true, true, true, false, false, true],
        };

        // Here we accessed the booleans propery 
        // of jsonBooleanArray Object.
        // It returned an boolean array. Then we accessed the
        // first index of the array
        // (which is true) using [] syntax.
        var x = jsonBooleanArray.booleans[0];
        // Set the inner HTML of "para" paragraph 
        // to the value of variable "x". 
        document.getElementById("para").innerHTML = x;
    </script>
</body>

</html>
```