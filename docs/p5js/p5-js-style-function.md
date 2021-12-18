# p5.js | style()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-style-function/](https://www.geeksforgeeks.org/p5-js-style-function/)

**样式()功能**用于设置给定值元素的样式属性。如果此函数包含单个参数，则使用。函数返回给定属性的值。

注意:这个函数需要 p5.dom 库。因此，在 index.html 文件的头部添加下面一行。

**语法:**

```
style( property )
```

或者

```
style( property, value )
```

**参数:**

*   **属性:**此参数保存 CSS 属性名称。
*   **值:**此参数保存 CSS 属性的值。

**返回值:**该函数返回属性值。

**例 1:**

```
function setup() {

    // Create canvas of size 400*200 
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

**例 2:**

```
function setup() {

    // Create canvas of size 400*200 
    createCanvas(400, 200);

    // Set background color
    background('green');

    // Create an input element
    var div_cont = createDiv('Welcome to GeeksforGeeks');

    // Set the position of div element
    div_cont.position(60, 80); 

    // Set the font color
    div_cont.style('color', '#ffffff');  

    // Set width of input field
    div_cont.style('width', '250px');

    // Set font-size of input text
    div_cont.style('font-size', '20px');

} 
```

**输出:**
![](img/81ac0e3caeecbad0cce4eb960619da61.png)