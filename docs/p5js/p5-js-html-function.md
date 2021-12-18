# p5.js | html()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-html-function/](https://www.geeksforgeeks.org/p5-js-html-function/)

**html()函数**用于通过替换任何现有的 html 来设置元素的内部 HTML。如果第二个参数的值为真，则追加 html，而不是替换现有的 html 元素。如果这个函数不包含任何参数，那么它返回元素的内部 HTML。

**注意:**这个函数需要 p5.dom 库。因此，在 index.html 文件的头部添加下面一行。

```
<script language="javascript" 
    type="text/javascript" src="path/to/p5.dom.js">
</script>
```

**语法:**

```
html()
```

或者

```
html( html, append )
```

**参数:**

*   **html:** 此参数保存字符串格式的 html 元素，需要放在元素内部。
*   **追加:**此参数保存布尔值以追加现有的 HTML 元素。

**返回值:**这个函数返回一个包含元素内部 HTML 的字符串。

下面的例子说明了 p5.js 中的 html()函数:

**例 1:**

```
function setup() {

    // Create a canvas of given size
    createCanvas(400, 200);

    // Set background color
    background('green');

    var div = createDiv('');

    // Use html() function
    div.html('Welcome to GeeksforGeeks');   

    // Set the position of div element
    div.position(60, 80); 

    // Set font-size of text
    div.style('font-size', '24px');

    // Set font-color of text
    div.style('color', 'white');

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

    var div = createDiv('').size(200, 70);

    // Use html() function    
    div.html('Welcome to GeeksforGeeks', true);   

    // Set the position of div element
    div.position(100, 60); 

    // Set font-size of text
    div.style('font-size', '24px');

    // Set font-color of text
    div.style('color', 'white');

    div.style('border', '1px solid white');

    div.style('text-align', 'center');

} 
```

**输出:**
![](img/a603eb0a65c8c519dfcab97dd5b98b94.png)