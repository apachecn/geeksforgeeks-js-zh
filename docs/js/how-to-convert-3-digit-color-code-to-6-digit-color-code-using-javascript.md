# 如何用 JavaScript 将 3 位色码转换成 6 位色码？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 将 3 位颜色代码转换为 6 位颜色代码/](https://www.geeksforgeeks.org/how-to-convert-3-digit-color-code-to-6-digit-color-code-using-javascript/)

在本文中，我们使用 JavaScript 将三位数的彩色 HEX 代码转换为六位数的彩色 HEX 代码。为了解决这个问题，我们首先在连续位置复制单个数字和贴纸。例如–**# 34E**将转换为 **#3344EE** 、 **#E90** 将转换为 **#EE9900。**

**将 3 位色码转换为 6 位色码的步骤:**

**第一步:**颜色代码为字符串格式。因此，对字符串应用 split 方法。应用拆分方法后，我们得到了一个元素数组。

## java 描述语言

```
<script>

var digit = "39E"

digit = digit.split("")

console.log(digit)

// ["#", "3", "9", "E"]
</script>
```

**输出:**

```
["#", "3", "9", "E"]
```

**第二步:**现在应用 map 方法，迭代数组，返回每个连接到自身的项，并检查该项是否为“#”，然后不返回连接结果，只返回该项。

## java 描述语言

```
<script>

var digit = "#39E";

digit = digit.split("").map((item)=>{
    if(item == "#"){return item}
        return item + item;
})

console.log(digit)

// ["#", "33", "99", "EE"]
</script>
```

**输出:**

```
["#", "33", "99", "EE"]
```

**步骤 3:** 现在使用 join 方法将所有数组项转换为单个字符串。

## java 描述语言

```
<script>

var digit = "#39E"

digit = digit.split("").map((item)=>{
    if(item == "#"){return item}
        return item + item;
}).join("")

console.log(digit)
<script>
```

**输出:**

```
"#3399EE"
```

**第四步:**在上面的步骤中，我们正在转换**“# 39E”**但是我们可以看到这个代码的第一个元素是**“#”，**但是如果用户没有提供**“#”**那么您必须检查第一个元素是否是“#”，然后将其与结果代码连接起来。这是我们的完整代码。

## java 描述语言

```
<script>

var digit = "#39E"

digit = digit.split("").map((item)=>{
    if(item == "#"){return item}
        return item + item;
}).join("")

if(digit[0] != "#"){
    digit = "#" + digit;
}

console.log(digit)
</script>
```

**输出:**

```
#3399EE
```