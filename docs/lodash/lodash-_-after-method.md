# 洛达什 _。()方法后

> 原文:[https://www.geeksforgeeks.org/lodash-_-after-method/](https://www.geeksforgeeks.org/lodash-_-after-method/)

**洛达什 _。after()** 方法与 **Lodash _ 相反。()前**法。此方法用于创建一个函数，该函数调用 func 次或更多次。

**语法:**

```
_.after(n, func)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **n:** This parameter stores n that defines the number of calls before calling func.
*   **Function:** This parameter stores the function to be called.

**返回值:**该方法返回新的受限函数。

下面的例子说明了 Lodash _。JavaScript 中的 after()方法。

**示例 1:** 在本例中，我们尝试调用函数 3 次，但它只会调用第 3 次。

```
// Requiring the lodash library  
const _ = require("lodash"); 

// Applying _.after() method
var gfg = _.after(3, function () {
  console.log('Saved');
});

gfg(); // Print nothing
gfg(); // Print nothing
gfg(); // Print Saved
```

**输出:**

```
Saved

```

**示例 2:** 在本例中，我们尝试调用函数 2 次，但它只会调用第 2 次。

```
// Requiring the lodash library  
const _ = require("lodash"); 

// Applying _.after() method
var gfg = _.after(2, function () {
  console.log('Successful');
});

gfg(); // Print nothing
gfg(); // Print Successful
```

**输出:**

```
Successful

```

**参考:**T2】https://docs-lodash.com/v4/after/