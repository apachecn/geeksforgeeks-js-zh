# 如何在 JavaScript 中用计算属性名声明对象？

> 原文:[https://www . geesforgeks . org/如何用 javascript 中的计算属性名称声明对象/](https://www.geeksforgeeks.org/how-to-declare-object-with-computed-property-name-in-javascript/)

在本文中，我们学习如何用计算属性名声明对象。在开始本文之前，我们必须了解 javascript 对象。

**Javascript 对象:** Javascript 对象包含键值对，其中键代表一个属性，我们可以从中获取和设置对象的值。现在我们将看到如何用计算属性名声明一个对象。

**方法 1:** 我们将使用[ ](方括号)中的表达式来创建对象属性的名称。在 ES6 中，可以在方括号“[ ]”中使用表达式。根据表达式的结果，属性名称将被分配给对象。

## Java Script 语言

```
<script>
    let LAST_NAME = "lastname";
    let fullname = {
        firstname: "somya",
        [LAST_NAME]: "jain"
    };
    console.log(
        "My fullname is: " + fullname.firstname
            + " " + fullname.lastname
    );
</script>
```

**输出:**

```
My fullname is: somya jain
```

**方法 2:** 在这个方法中，我们将动态创建一个对象的属性名。作为该方法的一部分，我们将动态创建一个对象，添加一个属性名，并为该特定属性赋值，以便创建一个自定义的键值对。

**语法:**

```
objectname["name of the property name"]=value

```

## java 描述语言

```
<script>
    let LAST_NAME = "lastname";
    let fullname = {
        firstname: "somya"
    };
    fullname[LAST_NAME] = "jain";
    console.log(
        "My fullname is: " + fullname.firstname
            + " " + fullname.lastname
    );
</script>
```

**输出:**

```
My fullname is: somya jain
```