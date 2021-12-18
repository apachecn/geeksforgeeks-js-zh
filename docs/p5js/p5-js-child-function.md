# p5.js | child()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-child-function/](https://www.geeksforgeeks.org/p5-js-child-function/)

**子()函数**用于将元素作为子元素添加到父元素中。这个函数接受字符串标识、DOM 节点或 p5.Element。如果这个函数不包含任何参数，那么它返回一个子 DOM 节点数组。

**注意:**这个函数使用 p5.dom 库。因此，在 index.html 文件的头部添加下面一行。

```
<script language="javascript" 
    type="text/javascript" src="path/to/p5.dom.js">
</script>
```

**语法:**

```
child()
```

或者

```
child( child )
```

**参数:**该函数接受单个参数**子**，它保存字符串或 p5 . element . ID、DOM 节点或 P5。元素用于作为当前元素添加。

**返回值:**返回子节点数组。

下面的例子说明了 p5.js 中的 child()函数:

**示例:**

```
function setup() {  

    // Create Canvas of given size 
    var cvs = createCanvas(600, 250);
}

function draw() {

    // Set the background color
    background('green'); 

    // Use createDiv() function to
    // create a div element
    var myDiv = createDiv('GeeksforGeeks');

    var myDiv1 = createDiv('A computer science portal for geeks');

    // Use child() function
    myDiv.child(myDiv1);

    // Set the position of div element
    myDiv.position(150, 100);  

    myDiv.style('text-align', 'center');

    // Set the font-size of text
    myDiv.style('font-size', '24px');

    // Set the font color
    myDiv.style('color', 'white');

}
```

**输出:**
![](img/d068cfe3d48a007ff2f7e753065d53f0.png)