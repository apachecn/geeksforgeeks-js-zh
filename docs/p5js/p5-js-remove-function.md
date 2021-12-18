# p5.js | remove()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-remove-function/](https://www.geeksforgeeks.org/p5-js-remove-function/)

**remove()函数**是一个内置函数，用于移除元素并取消注册所有侦听器。

这个函数需要 p5.dom 库。所以在**index.html**文件的头部增加下面一行。

```
<script language="javascript"
    type="text/javascript" src="path/to/p5.dom.js">
</script>
```

**语法:**

```
remove()
```

**参数:**此功能不接受任何参数。

下面的例子说明了 p5.js 中的 remove()函数:

**示例 1:** 本示例创建一个元素。

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
  var myDiv = createDiv('Welcome to GeeksforGeeks');

  // Set the position of div element
  myDiv.position(150, 100);  

  // Set the font-size of text
  myDiv.style('font-size', '24px');

  // Set the font color
  myDiv.style('color', 'white');

  // Comment the remove() function 
  // myDiv.remove();
}
```

**输出:**
![](img/d2f3389ebaf6053e9df0b1c93217305b.png)

**示例 2:** 本示例使用 remove()函数移除元素。

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
  var myDiv = createDiv('Welcome to GeeksforGeeks');

  // Set the position of div element
  myDiv.position(150, 100);  

  // Set the font-size of text
  myDiv.style('font-size', '24px');

  // Set the font color
  myDiv.style('color', 'white');

  // Use remove() function to remove div element
  myDiv.remove();
}
```

**输出:**
![](img/a9bb35d1d626a113e898efe968124a48.png)