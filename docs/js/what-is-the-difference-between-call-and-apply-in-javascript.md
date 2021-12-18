# 在 JavaScript 中调用和应用有什么区别？

> 原文:[https://www . geesforgeks . org/JavaScript 调用和应用的区别是什么/](https://www.geeksforgeeks.org/what-is-the-difference-between-call-and-apply-in-javascript/)

**调用()方法:**它调用方法，以所有者对象为参数。关键字这指的是函数或其所属对象的“所有者”。我们可以调用一个可以在不同对象上使用的方法。

**语法:**

```
object.objectMethod.call( objectInstance, arguments )
```

**参数:**它接受上面提到的和下面描述的两个参数:

*   **objectInstance:** 它保存一个对象的实例。
*   **参数:**call()方法采用逗号分隔的参数。

**apply()方法:**apply()方法用于编写方法，可以在不同的对象上使用。它不同于函数调用()，因为它将参数作为数组。
**语法:**

```
object.objectMethod.apply(objectInstance, arrayOfArguments)
```

**参数:**它接受上面提到的和下面描述的两个参数:

*   **objectInstance:** 它保存一个对象的实例。
*   **arrayOfArguments:**apply()方法采用参数数组。

**call()和 apply()方法的区别:**唯一的区别是 **call()** 方法采用逗号分隔的参数，而 **apply()** 方法采用参数数组。

**示例 1:** 本示例使用 call()方法调用函数。

```
<!DOCTYPE html>  
<html>
    <head>
        <title>call() method</title>
    </head>

    <body style = "text-align:center;">
        <h1 style = "color:green;" >  
            GeeksForGeeks  
        </h1>

        <button onClick="fun()">
            click
        </button>

        <p id="GFG"></p>

        <!-- Script to use call() method to call
            function -->
        <script>
            function fun() {
              let p = {
                fullName: function(addr1, addr2) {
                  return this.fName + " " + this.lName 
                        + ", " + addr1 + ", " + addr2;
                }
              }

              let p1 = {
                fName:"GFGfName",
                lName: "GFGlName",
              }

              let x = p.fullName.call(p1, "India", "USA"); 
              document.getElementById("GFG").innerHTML = x;
              }
        </script> 
    </body>
</html>
```

**输出:**

*   **点击按钮前:**
    ![](img/d62a4f46c6af7129acc84c2ffd8e3e78.png)
*   **After clicking the button:**
    ![](img/eaf86e375a0c9537b9473bcf123a46ee.png)
    **Example 2:**

    ```
    <!DOCTYPE html>  
    <html>  
        <head> 
            <title>JavaScript apply() method</title>
        </head> 

        <body style = "text-align:center;">  

            <h1 style = "color:green;" >  
                GeeksForGeeks  
            </h1> 

            <button onClick="fun()">
                click
            </button>

            <p id="GFG"></p> 

            <script>
                function fun() {
                    let p = {
                    fullName: function(addr1, addr2) {
                        return this.fName + " " + this.lName
                                + ", " + addr1 + ", " + addr2;
                    }
                }
                let p1 = {
                    fName:"GFGfName",
                    lName: "GFGlName",
                }
                    let x = p.fullName.apply(p1, ["India", "USA"]); 
                    document.getElementById("GFG").innerHTML = x;
                }
            </script> 
        </body>  
    </html>
    ```

    **输出:**

    *   **点击按钮前:**
        ![](img/d62a4f46c6af7129acc84c2ffd8e3e78.png)
    *   **点击按钮后:**
        ![](img/eaf86e375a0c9537b9473bcf123a46ee.png)