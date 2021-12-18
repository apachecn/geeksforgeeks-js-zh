# JavaScript | Intl。listformat . prototype . resolved options()方法

> 原文:[https://www . geesforgeks . org/JavaScript-intl-list format-prototype-resolved options-method/](https://www.geeksforgeeks.org/javascript-intl-listformat-prototype-resolvedoptions-method/)

**国际号码。ListFormat . prototype . resolved options()**方法是 JavaScript 中的一个内置方法，它返回一个新的对象，该对象的属性反映了在当前 ListFormat 对象的构造过程中计算出的区域设置和样式格式选项。
**语法:**

```
listFormat.resolvedOptions()
```

**参数:**此方法不接受任何参数。
**返回值:**该方法返回一个对象，该对象的属性反映了在构造给定列表格式对象期间计算的区域设置和格式选项。
以下示例说明了 Intl。JavaScript 中的 listformat . prototype . resolved options()方法:
**示例 1:**

## java 描述语言

```
<script>
const geeks = new Intl.ListFormat("de-DE", { style: "short" });

const result = geeks.resolvedOptions();
console.log(result.locale);
console.log(result.style); 
console.log(result.type);
</script>
```

**输出:**

```
"de"
"short"
"conjunction"
```

**例 2:**

## java 描述语言

```
<script>
const geeks = new Intl.ListFormat("hi");

const result = geeks.resolvedOptions();
console.log(result.locale);
console.log(result.style); 
console.log(result.type);
console.log(result.collation);
console.log(result.numeric);
</script>
```

**输出:**

```
"hi"
"long"
"conjunction"
undefined
undefined
```

**支持的浏览器:**Intl 支持的浏览器。方法如下:

*   谷歌 Chrome 72 及以上
*   边缘 79 及以上
*   Firefox 78 及以上版本
*   歌剧 60 及以上
*   Safari 14.1 及以上版本