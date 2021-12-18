# 如何用 JavaScript 打破嵌套 for 循环？

> 原文:[https://www . geesforgeks . org/how-break-nested for-loop-use-JavaScript/](https://www.geeksforgeeks.org/how-to-break-nested-for-loop-using-javascript/)

break 语句，用于提前退出循环。
一个标签可以与一个断点一起使用，以更精确地控制流量。**标签**只是一个标识符，后跟一个冒号(:)，用于一条语句或一段代码。

**注意:**在标签名和相关循环之间不应有任何其他语句。

**示例-1:** 从嵌套循环断开

```
<!DOCTYPE html>

<html>

<head>
    <title>
        Break Nested For loop
    </title>
</head>

<body>
    <script type="text/javascript">
        <!--
        document.write(
          "Entering the Geeks For Geeks!<br /> ");

        for (var i = 0; i < 5; i++) {
            document.write(
              "For Upper Level in GfG : " + i + "<br />");
            document.write("<br />")

            for (var j = 0; j < 5; j++) {
                // Break from the inner loop
                if (j == 3) break; 

                document.write(
                  "For Deeper Level in GfG : " + j + " <br />");
            }
           // Break from the outer loop
            if (i == 3) break;
        }
        document.write("Exiting the Geeks For Geeks!<br /> ");

    </script>
</body>
</html
```

**输出:**

```
Entering the Geeks For Geeks!
For Upper Level in GfG : 0

For Deeper Level in GfG : 0 
For Deeper Level in GfG : 1 
For Deeper Level in GfG : 2 
For Upper Level in GfG : 1

For Deeper Level in GfG : 0 
For Deeper Level in GfG : 1 
For Deeper Level in GfG : 2 
For Upper Level in GfG : 2

For Deeper Level in GfG : 0 
For Deeper Level in GfG : 1 
For Deeper Level in GfG : 2 
For Upper Level in GfG : 3

For Deeper Level in GfG : 0 
For Deeper Level in GfG : 1 
For Deeper Level in GfG : 2 
Exiting the Geeks For Geeks!

```

**示例-2:** 使用**标签**从嵌套循环中断开。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Break Nested For loop Using Labels
    </title>
</head>

<body>
    <script type="text/javascript">
        <!--
        document.write("Entering the Geeks for Geeks!<br /> ");
        upperloop: // This is the label name         
            for (var i = 0; i < 5; i++) {
                document.write(
                   "For Upper Level in GfG : " + i + "<br />");
                document.write("<br />");
                deeperloop:
                    for (var j = 0; j < 5; j++) {
                        // Break from the inner loop
                        if (j > 3) break; 
                        // Do the same thing
                        if (i == 2) break deeperloop; 
                        // Break from the outer loop
                        if (i == 3) break upperloop; 
                        document.write("For Deeper Level in GfG: "
                                       + j + " <br />");
                    }
            }
        document.write("Exiting the Geeks For Geeks!<br /> ");

    </script>
</body>

</html>
```

**输出:**

```
Entering the Geeks for Geeks!
For Upper Level in GfG : 0

For Deeper Level in GfG: 0 
For Deeper Level in GfG: 1 
For Deeper Level in GfG: 2 
For Deeper Level in GfG: 3 
For Upper Level in GfG : 1

For Deeper Level in GfG: 0 
For Deeper Level in GfG: 1 
For Deeper Level in GfG: 2 
For Deeper Level in GfG: 3 
For Upper Level in GfG : 2

For Upper Level in GfG : 3

Exiting the Geeks For Geeks!

```