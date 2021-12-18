# 洛达什 _。链()法

> 原文:[https://www.geeksforgeeks.org/lodash-_-chain-method/](https://www.geeksforgeeks.org/lodash-_-chain-method/)

**洛达什 _。chain()** 方法，用于在启用显式方法链序列的情况下包装值。

**语法:**

```
_.chain(value)

```

**参数:**该方法接受单个 a 参数，如上所述，如下所述:

*   **Value:** This parameter stores the value to be packaged.

**返回值:**此方法返回包装值。

下面的例子说明了 Lodash _。JavaScript 中的 chain()方法:

**例 1:**

## Javascript

```
const _ = require('lodash'); 

var person = [
  { 'user': 'Tommy',  'income': 2600 },
  { 'user': 'Asmita',    'income': 2400 },
  { 'user': 'Hiyan', 'income': 2200 }
];

var Earcning = _
  .chain(person)
  .sortBy('income')
  .map(function(gfg) {
    return gfg.user + ' earn is ' + gfg.income;
  })
  .value();
console.log(Earcning)
```

**输出:**

```
Hiyan earn is 2200,
Asmita earn is 2400,
Tommy earn is 2600

```

**例二:**

## Javascript

```
const _ = require('lodash'); 

var users = [
  { 'user': 'Tommy',  'age': 23 },
  { 'user': 'Asmita',    'age': 24 },
  { 'user': 'Hiyan', 'age': 22 }
];

var youngest = _
  .chain(users)
  .sortBy('age')
  .map(function(o) {
    return o.user + ' is ' + o.age;
  })
  .tail()
  .value();
console.log(youngest)
```

**输出:**

```
Tommy is 23,Asmita is 24

```

**参考:**T2】https://docs-lodash.com/v4/chain/