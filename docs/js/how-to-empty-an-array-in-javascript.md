# 如何在 JavaScript 中清空数组？

> 原文:[https://www . geesforgeks . org/如何清空 javascript 中的数组/](https://www.geeksforgeeks.org/how-to-empty-an-array-in-javascript/)

JavaScript 中有许多清空数组的方法，下面讨论其中一些:

**方法 1:设置为新数组:**这个方法将数组变量设置为大小为零的新数组，那么它将完美工作。

**示例:**

```
<!DOCTYPE html>  
<html>  

<head> 
    <title> 
        JavaScript to set array empty
    </title>
</head> 

<body style = "text-align:center;">  

    <h1 style = "color:green;" >  
        GeeksForGeeks  
    </h1>  

    <p id = "up"></p>

    <button onclick="empty()"> 
        Click to Empty
    </button> 

    <p id = "down" style="color: green"></p>

    <!-- Script to set size of array to zero -->
    <script> 
        var GFG_Array = [1, 2, 3, 4, 5];
        var up = document.getElementById("up");
        up.innerHTML = GFG_Array;
        var down = document.getElementById("down");
        down.innerHTML = "length of GFG_Array = "
                + GFG_Array.length;
        function empty() {
            GFG_Array = [];
            down = document.getElementById("down");
            down.innerHTML = "length of GFG_Array = "
                    + GFG_Array.length;
        }
    </script> 
</body>  

</html>
```

**输出:**

*   **点击按钮前:**
    ![](img/346a7d3092a124f208c0dd21c572787f.png)
*   **点击按钮后:**
    ![](img/79616b7bf11b3229e630eba2b5620c6c.png)

**方法二:使用长度属性:**该方法将数组的长度设置为零。

**示例:**

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        Create empty array
    </title>
</head> 

<body style = "text-align:center;"> 

    <h1 style = "color:green;" > 
        GeeksForGeeks 
    </h1> 

    <p id="up"></p>

    <button onclick="empty()"> 
        Click to Empty
    </button> 

    <p id="down" style="color: green"></p>

    <!-- Script to set the size of array to zero -->
    <script> 
        var GFG_Array = [1, 2, 3, 4, 5];
        var up = document.getElementById("up");
        up.innerHTML = GFG_Array;
        var down = document.getElementById("down");
        down.innerHTML = "length of GFG_Array = "
                + GFG_Array.length;

        function empty() {
            GFG_Array.length = 0;
            down = document.getElementById("down");
            down.innerHTML = "length of GFG_Array = "
                    + GFG_Array.length;
        }
    </script> 
</body> 

</html>                    
```

**输出:**

*   **点击按钮前:**
    ![](img/346a7d3092a124f208c0dd21c572787f.png)
*   **点击按钮后:**
    ![](img/79616b7bf11b3229e630eba2b5620c6c.png)

**方法三:使用 pop 方法:**该方法连续弹出数组元素，得到空数组。但是这种方法比其他方法花费更多的时间，并且不太受欢迎。
T3】例:

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        Create empty array
    </title>
</head>

<body style = "text-align:center;"> 

    <h1 style = "color:green;" > 
        GeeksForGeeks 
    </h1> 

    <p id="up"></p>

    <button onclick="empty()"> 
        Click to Empty
    </button> 

    <p id="down" style="color: green"></p>

    <!-- Script to set the size of array to zero -->    
    <script> 
        var GFG_Array = [1, 2, 3, 4, 5];
        var up = document.getElementById("up");
        up.innerHTML = GFG_Array;
        var down = document.getElementById("down");
        down.innerHTML = "length of GFG_Array = "
                + GFG_Array.length;

        function empty() {
            while(GFG_Array.length > 0) {
                GFG_Array.pop();
            }
            down = document.getElementById("down");
            down.innerHTML = "length of GFG_Array = "
                    + GFG_Array.length;
        }
    </script> 
</body> 

</html>                    
```

**输出:**

*   **点击按钮前:**
    ![](img/346a7d3092a124f208c0dd21c572787f.png)
*   **点击按钮后:**
    ![](img/79616b7bf11b3229e630eba2b5620c6c.png)