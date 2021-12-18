# p5.js |属性()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-attribute-function/](https://www.geeksforgeeks.org/p5-js-attribute-function/)

**属性()函数**用于在指定元素上添加新属性或更改现有属性的值。如果属性没有指定任何值，则返回给定属性的值，如果属性未设置，则返回 null。

**注意:**这个函数需要 p5.dom 库。因此，在 index.html 文件的头部添加下面一行。

**语法:**

```
attribute()
```

或者

```
attribute( attr, value )
```

**参数:**

*   **attr:** 该参数保存需要设置的属性名称。
*   **值:**该参数保存分配给该属性的值。

**返回值:**该函数以字符串形式返回属性值。

下面的例子说明了 p5.js 中的 attribute()函数:

**示例:**

```
function setup() {

    // Canvas size 400*400 
    createCanvas(400, 200);

    // Set background color
    background('green');

    // Create an input element
    var input_val = createInput('');    

    // Set the attribute and its value    
    input_val.attribute('value', 'Welcome to GeeksforGeeks');  

    // Set the position of div element
    input_val.position(60, 80); 

    // Set width of input field
    input_val.style('width', '250px');

    // Set font-size of input text
    input_val.style('font-size', '20px');
} 
```

**输出:**
![](img/9d03b234f2a94c37a4b21fba032e5fff.png)