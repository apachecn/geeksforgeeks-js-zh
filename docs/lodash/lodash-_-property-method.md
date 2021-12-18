# 洛达什 _。属性()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-property-method/](https://www.geeksforgeeks.org/lodash-_-property-method/)

洛达什 **_。property()** 方法用于返回一个函数，该函数将返回任何传入对象的指定属性。

**语法:**

```
_.property(path)

```

**参数:**该方法接受一个参数，如上所述，如下所述:

*   **路径:**此参数保存要获取的属性的路径。

**返回值:**这个方法返回一个新的访问器函数。

**例 1 :**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");            

var info = { 
            Company: 'GeeksforGeeks', 
            Address: 'Noida'
        }; 

// Use of _.property() method         
let gfg = _.property('Company')
        (info) === 'GeeksforGeeks' 

// Printing the output  
console.log(gfg);
```

**输出:**

```
true

```

**例 2 :**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");            

var info = { 
            Company: { name: 'GeeksforGeeks' }, 
            Contact: { Address:  
                {  
                    AddressInfo: 'Noida'  
                }  
            } 
        }; 

// Use of _.property() method  
 var propInfo = _.property(['Contact', 
         'Address', 'AddressInfo', ]); 

// Printing the output  
console.log(propInfo(info));
```

**输出:**

```
Noida

```