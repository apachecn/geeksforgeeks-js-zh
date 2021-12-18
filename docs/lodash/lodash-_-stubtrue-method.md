# 洛达什 _。stubTrue()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-stubtrue-method/](https://www.geeksforgeeks.org/lodash-_-stubtrue-method/)

洛达什 **_。stubTrue()方法**用于返回一个**真**值。当它被调用时，它总是返回**真**。

**语法:**

```
_.stubTrue()
```

**参数:**此方法不接受任何单个参数。

**返回值:**返回真值。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");            

// Use of _.stubTrue() method 
let gfg = _.stubTrue(); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
true
```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");            

for(let i = 0; i < 10; i++){
    // Printing the output  
    console.log( _.stubTrue() );
}
```

**输出:**

```
true
true
true
true
true
true
true
true
true
true

```