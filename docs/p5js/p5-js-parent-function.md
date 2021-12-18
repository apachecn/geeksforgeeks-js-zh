# p5.js parent()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-parent-function/](https://www.geeksforgeeks.org/p5-js-parent-function/)

parent()函数用于将元素附加为父元素。该函数接受字符串标识、DOM 节点或 p5.Element。如果父节点不包含任何参数，则该函数返回父节点。

**语法:**

```
parent( parent )
```

或者

```
parent()
```

**参数:**包含单参数**父级**，保存字符串 p5。元素对象作为元素。

下面的例子说明了 p5.js 中的 parent()函数:

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

    // Use parent() function
    myDiv1.parent(myDiv);

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