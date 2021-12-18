# 洛达什 _。延迟()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-delay-method/](https://www.geeksforgeeks.org/lodash-_-delay-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。delay()方法**用于在规定的等待时间结束后调用给定的函数作为参数，以毫秒为单位。调用函数时，会向函数提供任何进一步的参数。

**语法**:

```
_.delay( func, wait, args )
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **功能:**就是要延迟的功能。
*   **wait:** 是函数调用延迟的毫秒数。
*   **参数:**是调用给定函数的参数。这是一个可选参数。

**返回值:**该方法返回定时器 id。

**示例 1:** 在该示例中，由于等待时间为 3 秒，因此在延迟 3 秒后打印内容。

## java 描述语言

```
// Requiring lodash library
const _ = require('lodash');

// Using the _.delay() method
// with its parameter
_.delay(function(content) {
    console.log(content);
  }, 3000, 'GeeksforGeeks!');

// Print the content after this line
console.log('Content:');
```

**输出:**

```
Content:
GeeksforGeeks!
```

**例 2:** 在本例中，每个整数在延迟 2 秒后打印。

## java 描述语言

```
// Requiring lodash library
const _ = require('lodash');

// Defining func parameter
let func = number => {
  console.log(number);
};

// Defining for loop
for(let i = 1; i <= 5; i++) {

    // Using the _.delay() method
    // with its parameter
    _.delay(func, 2000 * (i + 1), i);
}

// Prints the integer after this line
console.log('Integers are as follows:');
```

**输出:**

```
Integers are as follows:
1
2
3
4
5
```