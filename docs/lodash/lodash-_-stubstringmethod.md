# 洛达什 _。stubString()方法

> [https://www.geeksforgeeks.org/lodash-_-stubstringmethod/](https://www.geeksforgeeks.org/lodash-_-stubstringmethod/)

洛达什 **_。stubString()方法**用于创建空字符串。

**语法:**

```
_.stubString()
```

**参数:**此方法不接受任何参数。

**返回值:**这个方法返回一个空字符串。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");            

// Use of _.stubString() method 
// to create an empty String
let gfg = _.stubString(); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
""

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");            

// Use of _.stubString() method 
// to create 5 empty String
let gfg = _.times(5, _.stubString); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
["", "", "", "", ""]

```