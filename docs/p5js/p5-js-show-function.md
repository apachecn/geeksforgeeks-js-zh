# p5.js | show()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-show-function/](https://www.geeksforgeeks.org/p5-js-show-function/)

**显示()功能**是一个内置功能，用于显示当前元素。使用设置**显示:出于风格目的阻止**。

这个函数需要 p5.dom 库。所以在**index.html**文件的头部增加下面一行。

```
<script language="javascript" 
    type="text/javascript" src="path/to/p5.dom.js">
</script>
```

**语法:**

```
show()
```

**参数:**此功能不接受任何参数。

下面的例子说明了 p5.js 中的 show()函数:

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
  var myDiv1 = createDiv('GeeksforGeeks');

  // Set the position of div element
  myDiv1.position(170, 30);  

  // Set the div size
  myDiv1.size(200, 100);

  // Set the font-size of text
  myDiv1.style('font-size', '36px');

  // Use createDiv() function to
  // create a div element
  var myDiv = createDiv('A computer science portal for geeks');

  // Set the position of div element
  myDiv.position(180, 80);  

  // Set the div size
  myDiv.size(200, 100);

  // Set the font-size of text
  myDiv.style('font-size', '24px');

  // Set the font-size of text
  myDiv.style('border', '1px solid black');

  // Set the font-size of text
  myDiv.style('text-align', 'center');

  // Set the font color
  myDiv.style('color', 'white');

  // Hide the div element
  myDiv.hide();

  // Show the div element
  myDiv.show();
}
```

**输出:**
![show() function](img/d9067127e1188ca64e0875f90c0cfc64.png)