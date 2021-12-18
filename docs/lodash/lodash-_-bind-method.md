# 洛达什 _。绑定()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-bind-method/](https://www.geeksforgeeks.org/lodash-_-bind-method/)

**洛达什 _。bind()** 方法用于创建一个函数，该函数将使用 **thisArg** 的 **this** 绑定来调用给定的函数，它用于将函数绑定到对象。当函数被调用时，它的值将是对象。****_ . bind . placeholder**值在整体构建中默认为 _ 可用作部分应用参数的占位符。**

****语法:****

```
_.bind(func, thisArg, partials) 
```

****参数:**该方法接受三个参数，如上所述，如下所述:**

***   **Function:** This parameter holds the function to be bound.*   **This parameter holds the object element.***   **Partitions:** This parameter needs to add some symbols between elements.**

****返回值:**这个方法返回一个新的边界函数。**

**下面的例子说明了 Lodash _。bind()方法:**

****例 1:****

## **Javascript**

```
// Acquiring lodash variable
const _ = require('lodash'); 

// Function
var fun = function(Geeks) { 
    return 'Company Name : ' + this.Company 
        + '\nAddress : ' + this.Address 
        + '\nContact : ' + this.Contact 
}; 

// Use of bind() function
var func = _.bind(fun, { 
    Company: 'GeeksforGeeks', 
    Address: 'Noida', 
    Contact: '+91 9876543210' 
}); 

console.log(func());
```

****输出:****

```
Company Name : GeeksforGeeks 
Address : Noida 
Contact : +91 9876543210 
```

****例二:****

## **Javascript**

```
// Lodash variable
const _ = require('lodash'); 

var obj = { 
    Name: "GeeksforGeeks", 
    Address: "Noida" 
}; 

var fun = function (Geeks) { 
    return 'Welcome to ' + this.Name 
        + '\nAddress: ' + this.Address 
};

var func = _.bind(fun, obj); 

console.log(func());
```

****输出:****

```
Welcome to GeeksforGeeks 
Address: Noida 
```

****参考:**T2】https://docs-lodash.com/v4/bind/**