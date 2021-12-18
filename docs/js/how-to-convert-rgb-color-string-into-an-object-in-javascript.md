# 如何在 JavaScript 中将 rgb()颜色字符串转换为对象？

> 原文:[https://www . geesforgeks . org/how-convert-RGB-color-string-in-object-in-JavaScript/](https://www.geeksforgeeks.org/how-to-convert-rgb-color-string-into-an-object-in-javascript/)

给定 rgb()或 rgba()形式的颜色，任务是将其转换为一个对象，其中键是颜色名称，值是颜色值。

#### **示例:**

```
Input:    rgb(242, 52, 110)
Output: {
   red: 242,
   green: 52,
   blue: 110
}

Input:    rgba(255, 99, 71, 0.5)
Output: {
  red: 255,
  green: 99,
  blue: 71,
  alpha: 0.5
}
```

**方法:**为了实现这一点，我们使用以下方法。

*   将颜色存储在一个名为 rgb 的变量中。
*   创建一个名为 colors 的数组，其中包含红色、绿色、蓝色和 alpha 颜色的名称。
*   创建一个名为 colorArr 的变量，我们在其中存储输入 rgb 的颜色值。例如:**[“255”，“99”，“71”，0.5]，**要实现这一点我们**把**的 rgb 从**所在的地方“(“**呈现到从**”**呈现的地方。现在你得到了字符串**“255，99，71，0.5”。**现在从**、“**出现的地方分割阵列。现在你得到数组**[“255”、‘99’、‘71’、‘0.5”]。**
*   现在创建一个空对象。
*   在 colorArr 上应用 forEach 循环，并为每次迭代向对象插入颜色名称和颜色值。
*   现在打印对象。

## java 描述语言

```
<script>
let rgb = "rgba(255, 99, 71, 0.5)"

let colors = ["red", "green", "blue", "alpha"]

// Getting the index of "(" and ")" 
// by using the indexOf() method
let colorArr = rgb.slice(
    rgb.indexOf("(") + 1, 
    rgb.indexOf(")")
).split(", ");

let obj = new Object();

// Insert the values into obj
colorArr.forEach((k, i) => {
    obj[colors[i]] = k
})

console.log(obj)
</script>
```

**输出:**

```
{
 alpha: "0.5",
 blue: "71",
 green: "99",
 red: "255"
}
```

#### **将逻辑包装在函数内**

## java 描述语言

```
<script>
function rgbToObj(rgb) {

    let colors = ["red", "green", "blue", "alpha"]

    let colorArr = rgb.slice(
        rgb.indexOf("(") + 1, 
        rgb.indexOf(")")
    ).split(", ");

    let obj = new Object();

    colorArr.forEach((k, i) => {
        obj[colors[i]] = k
    })

    return obj;
}

console.log(rgbToObj("rgb(255, 99, 71)"))
console.log(rgbToObj("rgb(255, 99, 71, 0.5)"))
</script>
```

**输出:**

```
{
 blue: "71",
 green: "99",
 red: "255"
}

{
 alpha: "0.5",
 blue: "71",
 green: "99",
 red: "255"
}
```