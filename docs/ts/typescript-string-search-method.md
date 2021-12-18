# 类型脚本|字符串搜索()方法

> 原文:[https://www . geesforgeks . org/typescript-string-search-method/](https://www.geeksforgeeks.org/typescript-string-search-method/)

**搜索()**是 TypeScript 中的一个内置函数，用于搜索正则表达式和该字符串对象之间的匹配。
**语法:**

```
string.search(regexp);
```

**参数:**这些方法接受如上所述的单个参数，如下所述:

*   **regexp:** 这个参数是一个 regexp 对象。

**返回值:**这个方法返回字符串内部正则表达式的索引。否则，它返回-1。
以下示例说明了打字稿中的**字符串搜索()**方法:

**例 1:**

## java 描述语言

```
// This is TypeScript
// Original strings
var str = "Geeksforgeeks - Best Platform";

var re = /Best/gi;

// use of String search() Method
if (str.search(re) == -1 ) {
  console.log("Not Found" );
} else {
  console.log("Found" );
}
```

**输出:**

```
Found
```

**例 2:**

## Java Script 语言

```
// This is TypeScript
// Original strings
var str = "Geeksforgeeks - Best Platform";

var re = /geeek/gi;

// use of String search() Method
if (str.search(re) == -1 ) {
    console.log("Not Found" );
} else {
    console.log("Found" );
}
```

**输出:**

```
Not Found 
```