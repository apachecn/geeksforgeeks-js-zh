# 洛达什 _。isRegExp()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isregexp-method/](https://www.geeksforgeeks.org/lodash-_-isregexp-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。isRegExp()方法**用于查找给定值是否为正则表达式。如果给定值是正则表达式，则返回真。否则，它返回 false。

**语法:**

```
_.isRegExp(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

**值:**该参数保存要检查的值。

**返回值:**如果值是正则表达式，则该方法返回 true，否则返回 false。

**注意:**这里，const _ = require('lodash ')用于将 lodash 库导入文件。
**示例 1:** **将正则表达式传递给 _。isRegExp()函数**
这里，对象以“/”开头和结尾，因此是正则表达式。因此，结果是真的。

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Use of _.isRegExp() method
console.log(_.isRegExp(/gfg/));
```

**输出:**

```
true
```

**示例 2:** **将字符串传递给 _。函数**
由于字符串不是正则表达式，因此输出为假。

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Use of _.isRegExp() method
console.log(_.isRegExp('gfg'));
```

**输出:**

```
false
```

**示例 3:** **传递一个带“/”的字符串到 _。isRegExp()函数**
因此整体对象是一个字符串。，输出将为假。

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Use of _.isRegExp() method
console.log(_.isRegExp('/gfg/'));
```

**输出:**

```
false
```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。

**参考:**T2https://lodash.com/docs/4.17.15#isRegExp