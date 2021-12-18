# p5.js |位置()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-position-function/](https://www.geeksforgeeks.org/p5-js-position-function/)

**位置()功能**用于设置元素相对于原点(0，0)坐标的位置。如果这个函数不包含任何参数，那么它返回元素的 x 和 y 位置。

**注意:**这个函数需要 p5.dom 库。因此，在 index.html 文件的头部添加下面一行。

```
<script language="javascript" 
    type="text/javascript" src="path/to/p5.dom.js">
</script>
```

**语法:**

```
position()
```

或者

```
position( x, y )
```

**参数:**

*   **x:** 该参数保持相对于窗口左上角的 x 位置。
*   **y:** 该参数保持相对于窗口左上角的 y 位置。

**返回值:**这个函数返回一个包含元素 x 和 y 位置的对象。

下面的例子说明了 p5.js 中的 position()函数:

**例 1:**

```
function setup() {

    // Create canvas of given size
    createCanvas(400, 200);

    // Set background color
    background('green');

    // Create an input element
    var div_cont = createDiv('Welcome to GeeksforGeeks');

    // Set the position of div element
    div_cont.position(60, 80); 

    // Set font color
    div_cont.style('color', '#ffffff');  

    // Set width of input field
    div_cont.style('width', '250px');

    // Set font-size of input text
    div_cont.style('font-size', '20px');

} 
```

**输出:**
![](img/81ac0e3caeecbad0cce4eb960619da61.png)

**例 2:**

```
function setup() {

    // Create canvas of given size
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