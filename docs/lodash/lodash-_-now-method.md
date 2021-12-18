# 洛达什 _。现在()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-now-method/](https://www.geeksforgeeks.org/lodash-_-now-method/)

**_。now()方法**用于获取自 Unix 纪元(1970 年 1 月 1 日 00:00:00 UTC)以来经过的毫秒数的时间戳。

**语法:**

```
_.now()
```

**参数:**此方法不接受任何参数。

**返回值:**该方法返回时间戳。

**例 1:**

## Javascript

```
// Defining Lodash variable
const _ = require('lodash');

// Getting the timestamp
console.log(_.now());
```

**输出:**

```
1599545119753

```

**例二:**

## Javascript

```
// Defining Lodash variable
const _ = require('lodash');

// Creating print function to print
// timestamp after delay of 10ms 
function print(){ 
    setTimeout(() => { 
        console.log(
`Current timestamp is: ${_.now()}`) 
    }, 10) 
} 

// Running this function 5 times
// using _.times() function. 
_.times(5, print) 
console.log("Type of timestamp is: ", 
    typeof(_.now())) 
```

**输出:**

```
Type of timestamp is:  number
Current timestamp is: 1599546710915
Current timestamp is: 1599546710916
Current timestamp is: 1599546710916
Current timestamp is: 1599546710916
Current timestamp is: 1599546710916

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash 库。