# JavaScript 错误()构造函数

> 原文:[https://www.geeksforgeeks.org/javascript-error-constructor/](https://www.geeksforgeeks.org/javascript-error-constructor/)

Javascript Error()构造函数用于创建新的[错误对象](https://www.geeksforgeeks.org/javascript-error-object-complete-reference/)。错误对象出现在运行时错误。错误对象还将用作用户定义的异常的基本对象。

**语法:**

```
new Error([message[, fileName[, lineNumber]]])
```

**参数:**

*   **消息:**它包含人类可读形式的关于该错误对象的信息。可以使用 [javascript 错误消息属性](https://www.geeksforgeeks.org/javascript-error-message-property/)设置错误消息。这是一个可选参数。
*   **文件名:**是这个错误对象的文件名。如果未提供名称，则 fileName 等于包含调用 Error()构造函数的代码的文件的名称。这是一个可选参数。
*   **行号:**是创建的错误对象的行号属性的值。如果未提供数字，则行号等于包含错误()构造函数调用的行号。这是一个可选参数。

**示例 1:** 使用新关键字创建错误对象。

## java 描述语言

```
<script>
try {
    const error = new Error('This object is created using new keyword')
    document.write("Error object created successfully using new keyword");
}
 catch(err) {
     document.write(err.message);
}
</script>
```

**输出:**

```
Error object created successfully using new keyword
```

**示例 2:** 使用函数调用创建错误对象。

## java 描述语言

```
<script>
try {
    const error =  Error('This is created is using function call')
    document.write("Error object created successfully using function call");
}
 catch(err) {
     document.write(err.message);
}
</script>
```

**输出:**

```
Error object created successfully using function call
```

**支持的浏览器:**

*   谷歌 Chrome
*   火狐浏览器
*   边缘
*   微软公司出品的 web 浏览器
*   歌剧
*   旅行队