# 类型脚本|字符串构造器属性

> 原文:[https://www . geesforgeks . org/typescript-string-constructor-property/](https://www.geeksforgeeks.org/typescript-string-constructor-property/)

[](https://www.geeksforgeeks.org/hello-world-in-typescript-language/)**中的**构造函数属性()**用于返回创建对象的字符串函数的引用。
**语法:****

```
string.constructor 
```

****返回值:**该方法返回对创建对象的 String 函数的引用。
以下示例说明了打字稿中的**字符串构造函数属性****

****例 1:****

## **Java Script 语言**

```
<script>
    // Original strings
    var str = "Geeksforgeeks - Best Platform"; 

    // use of Constructor Property
    var newstr = str.constructor 
    console.log("Return Value of constructor property:", newstr);
</script>
```