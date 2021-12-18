# 洛达什 _。isEqualWith()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isequalwith-method/](https://www.geeksforgeeks.org/lodash-_-isequalwith-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。*洛达士*中郎的法**与*相似。isEqual()* 方法，唯一不同的是它接受*定制器*，调用这个定制器是为了比较值。此外，如果此处使用的*定制器*返回未定义，则通过方法来处理比较。

**注意:**这里使用的*定制器*最多可以用 6 个参数调用，分别是 *objValue* 、 *othValue* 、*索引* | *键*、*对象*、*其他*、*堆栈*。

**语法:**

```
_.isEqualWith(value, other, [customizer])

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **Value:** is the value to be compared.
*   **Other:** is another value to be compared.
*   **Customizer:** is a function for customizing comparison.

**返回值:**如果所述值相等，则该方法返回真，否则返回假。

**例 1:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Defining a function portal
function portal(val) {
  return /^G(?:fG|eeksforGeeks)$/.test(val);
}

// Defining customizer to compare values
function customizer(objectValue, otherValue) {
  if (portal(objectValue) && portal(otherValue)) {
    return true;
  }
}

// Initializing values
var val = ['GeeksforGeeks', 'CS-portal'];
var otherval = ['GfG', 'CS-portal'];

// Calling isEqualWith() method with all
// its parameter
let result = _.isEqualWith(val, otherval, customizer); 

// Displays output
console.log(result);
```

**输出:**

```
true

```

**例二:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Defining a function portal
function portal(val) {
  return /^G(?:fG|eeksforGeeks)$/.test(val);
}

// Defining customizer to compare values
function customizer(objectValue, otherValue) {
  if (portal(objectValue) && portal(otherValue)) {
    return true;
  }
}

// Initializing values
var val = ['GeeksforGeeks', 'CS-portal'];
var otherval = ['GfG', 'portal'];

// Calling isEqualWith() method with all
// its parameter
let result = _.isEqualWith(val, otherval, customizer); 

// Displays output
console.log(result);
```

**输出:**

```
false

```

**例三:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Defining a function gfg
function gfg(val) {
  return val;
}

// Defining customizer
function intg(x, y) {
 if (gfg(x) === gfg(y)){  
  return true;
   }
}

// Calling isEqualWith() method with all
// its parameter
let result = _.isEqualWith('gf', 'gfg', intg); 

// Displays output
console.log(result);
```

**输出:**

```
false

```

**参考资料:**[https://lodash . com/docs/4 . 17 . 15 # isequal with](https://lodash.com/docs/4.17.15#isEqualWith)