# JavaScript | Intl。整理器.原型.解析选项()方法

> 原文:[https://www . geesforgeks . org/JavaScript-intl-collator-prototype-resolved options-method/](https://www.geeksforgeeks.org/javascript-intl-collator-prototype-resolvedoptions-method/)

**国际号码。Collator . prototype . resolved options()**方法是 JavaScript 中的内置方法，用于返回一个新对象，该对象的属性反映了在初始化此 Collator 对象期间计算的区域设置和排序规则选项。
**语法:**

```
collator.resolvedOptions()
```

**参数:**此功能不接受任何参数。
**返回值:**此方法返回一个新对象，其属性反映了在给定排序规则对象初始化期间计算的区域设置和排序规则选项。
以下示例说明了 **Intl 中的。collator . prototype . resolved options()方法** JavaScript:
**示例 1:**

## java 描述语言

```
var vall = new Intl.Collator('de', { sensitivity: 'base' })
var geek = vall.resolvedOptions();

console.log(geek.locale);          
console.log(geek.usage);       
console.log(geek.sensitivity);  
console.log(geek.ignorePunctuation);
console.log(geek.collation);        
console.log(geek.numeric);
```

**输出:**

```
"de"
"sort"
"base"
false
"default"
false
```

**例 2:**

## java 描述语言

```
let geek = new Intl.Collator('de-DE');
let geek1 = new Intl.Collator('ar');
let geek2 = new Intl.Collator('hi');
let val1 = geek.resolvedOptions();
let val2 = geek1.resolvedOptions();
let val3= geek2.resolvedOptions();
console.log(val1.sensitivity);
console.log(val2.collation);
console.log(val3.numeric);
```

**输出:**

```
"variant"
"default"
false
```

**支持的浏览器:**T2 国际机场支持的浏览器。整理器.原型.解析选项()方法如下:

*   谷歌 Chrome 24 及以上版本
*   Firefox 29 及以上版本
*   歌剧 15 及以上
*   边缘 12 及以上
*   IE 11 及以上
*   Safari 10 及以上