# 如何在 JavaScript 中将字符串的一部分替换为另一个值？

> 原文:[https://www . geesforgeks . org/如何用 javascript 中的另一个值替换部分字符串/](https://www.geeksforgeeks.org/how-to-replace-a-portion-of-strings-with-another-value-in-javascript/)

我们可以用多种方法替换字符串的一部分。下面用例子提到和描述流行的。

1.  [**JavaScript 替换()方法**](https://www.geeksforgeeks.org/javascript-replace-method/)
2.  [**Javascript split()方法**](https://www.geeksforgeeks.org/javascript-string-prototype-split-function/)
3.  [**Javascript 加入()方法**](https://www.geeksforgeeks.org/javascript-array-join-method/)

**JavaScript replace()方法:**我们可以用 **replace()** 方法替换一部分 String。JavaScript 有一个名为 replace 的内置方法，它允许您用另一个字符串或正则表达式替换字符串的一部分。但是，原始字符串将保持不变。

**语法:**

```
string.replace(searchvalue, newvalue)
```

第一个参数用于在整个字符串中搜索字符串，新字符串将替换搜索到的字符串。此函数返回一个新字符串，但原始字符串保持不变。

**例 1:**

## 超文本标记语言

```
<script>
    let string = "GeeksForGeeks";
    /* It first search 'For' in original string then it will 
    replace the searched string('For') with new string ('and') */

    let replaced_string = string.replace("For", "and");
    console.log("The original string is " + string);
    console.log("The replaced string is " + replaced_string);
</script>
```

**输出:**

```
The original string is GeeksForGeeks
The replaced string is GeeksandGeeks
```

我们也可以使用两个内置的 javascript 函数**拆分**和**将**函数连接在一起来完成这个任务。

**Javascript split()方法:**split 函数是一个 Javascript 内置函数，用于将字符串拆分为一个子字符串数组。此函数采用两个可选参数作为参数，如分隔符和限制。分隔符是字符串或属于原始字符串的任何字符。拆分是用这个字符(或正则表达式)完成的。如果省略此字符，原始字符串将作为数组返回。极限是一种整数类型，表示拆分的次数。

```
string.split(separator,limit)
```

**JavaScript join()方法:**join 函数是一个 JavaScript 内置函数，用于连接元素数组并将其作为字符串返回。此方法只有一个可选参数。

```
array.join(separator)
```

**示例 2:** 这里我们使用方法**链接**一次同时使用这两种方法。

## 超文本标记语言

```
<script>
    let string = "GeeksForGeeks";
    /* split method split the string into an 
       array(['Geeks','Geeks']) and the join method will 
       join the string with another string ('and') */

    let replaced_string = string.split("For").join("and");
    console.log("The replaced string is " + replaced_string);
    console.log("The original string is " + string);
</script>
```

**输出:**

```
The replaced string is GeeksandGeeks
The original string is GeeksForGeeks
```