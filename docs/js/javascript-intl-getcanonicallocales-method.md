# JavaScript | intl . getcanonicallcales()方法

> 原文:[https://www . geesforgeks . org/JavaScript-intl-getcanonicallocales-method/](https://www.geeksforgeeks.org/javascript-intl-getcanonicallocales-method/)

JavaScript 中的**intl . getcanonicallcales()方法**是一个标准的内置对象，它返回一个包含规范区域名称的数组。
**语法:**

```
Intl.getCanonicalLocales(locales)
```

**参数:**该方法接受上述单个参数，描述如下:

*   **区域设置:**此参数保存一个字符串值列表，从中可以获得规范的区域设置名称。

**返回值:**这个方法返回一个包含规范区域名称的数组。
以下示例说明了 JavaScript 中的 Intl.getCanonicalLocales()方法:
**示例 1:**

## java 描述语言

```
console.log(Intl.getCanonicalLocales('EN-US'));
console.log(Intl.getCanonicalLocales(['EN-US', 'Fr']));

try {
    Intl.getCanonicalLocales('GeeksforGeeks');
} catch (error) {
    console.log(error);
}
```