# p5.js | center()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-center-function/](https://www.geeksforgeeks.org/p5-js-center-function/)

**中心()功能**用于设置元素相对于其父元素垂直、水平或两者的中心对齐，如果元素没有父元素，则根据主体对齐。如果此函数不包含任何参数，则元素将垂直和水平对齐。

**注意:**这个函数需要 p5.dom 库。因此，在 index.html 文件的头部添加下面一行。

```
<script language="javascript"
    type="text/javascript" src="path/to/p5.dom.js">
</script>
```

**语法:**

```
center( align )
```

**参数:**该函数接受单个参数**对齐**，保持字符串“垂直”或“水平”对齐元素。

下面的例子说明了 p5.js 中的 center()函数:

**例 1:**

```
function setup() {

    // Create canvas of given size
    createCanvas(1000, 200);

    // Set background color
    background('green');

    var div = createDiv('').size(200, 70);

    div.html('Welcome to GeeksforGeeks', true);   

    // Set the position of div into center
    div.center();

    // Set font-size of text
    div.style('font-size', '24px');

    // Set font-color of text
    div.style('color', 'white');

    div.style('border', '1px solid white');

    div.style('text-align', 'center');

} 
```

**输出:**
![](img/53d672605fefde941f28761d40ece448.png)

**例 2:**

```
function setup() {

    // Create canvas of given size
    createCanvas(1000, 200);

    // Set background color
    background('green');

    // Create an input element
    var input_val = createInput('');    

    // Set the attribute and its value    
    input_val.attribute('value', 'Welcome to GeeksforGeeks');     

    // Set the position of div into center
    input_val.center();

    // Set font-size of text
    input_val.style('font-size', '24px');

    // Set the width of input area
    input_val.style('width', '300px');

} 
```

**输出:**
![](img/9d03b234f2a94c37a4b21fba032e5fff.png)