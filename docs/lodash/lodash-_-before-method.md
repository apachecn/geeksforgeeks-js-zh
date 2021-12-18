# 洛达什 _。之前()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-before-method/](https://www.geeksforgeeks.org/lodash-_-before-method/)

**洛达什 _。()**之前的方法是与**相反的洛达士 _。()后**法。此方法用于创建一个调用**函数**的函数，该函数具有**绑定和所创建函数的参数，但调用次数少于 **n** 。**

****语法:****

```
_.before(n, func) 
```

****参数:**该方法接受两个参数，如上所述，如下所述:**

***   **n:** This parameter holds the number n, which is used to define the number of calls for no longer calling func.*   **Function:** This parameter stores the function to be called.**

****返回值:**该方法返回新的受限函数。**

**下面的例子说明了 Lodash _。before()方法:**

****示例 1:** 在本例中，我们将尝试调用函数 3 次，但它只会调用 2 次。**

## **Javascript**

```
// Requiring the lodash library  
const _ = require("lodash");

// Using _.before() method
var gfg = _.before(3, function () {
    console.log('Saved');
});

// It will print Saved
gfg(); 

// It will print Saved
gfg();

// It will print nothing
gfg();
```

****输出:****

```
Saved
Saved 
```

****例二:****

## **Javascript**

```
// Requiring the lodash library  
const _ = require("lodash"); 

// Applying _.before() method
var gfg = _.before(2, function () {
     console.log('Successful');
});

// It will print Successful
gfg();

// It will print nothing
gfg();
```

****输出:****

```
Successful 
```

****参考:**T2】https://docs-lodash.com/v4/before/**