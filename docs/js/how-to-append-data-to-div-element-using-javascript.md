# 如何使用 JavaScript 向元素追加数据？

> 原文: [https://www .极客们。org/how-追加数据到 div-元素-使用-JavaScript/](https://www.geeksforgeeks.org/how-to-append-data-to-div-element-using-javascript/)

要将数据追加到< div >元素，我们必须使用[DOM(Document Object Model)](https://www.geeksforgeeks.org/dom-document-object-model/)操作技术。方法是在 HTML 框架中创建一个 id 为的空的< div >。然后那个 id 将被用来获取那个< div >，然后我们将操纵那个 div 的内部文本。

**语法:**

```
document.getElementById("div_name").innerText += "Your Data Here";
```

**示例:**

```
<!DOCTYPE html> 
<html> 

<head> 
    <title>
        How to append data to
        div using JavaScript ?
    </title> 

    <meta charset="utf-8"> 

    <meta name="viewport"
        content="width=device-width, initial-scale=1"> 

    <link rel="stylesheet" href= 
"https://maxcdn.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">

</head> 

<body> 
    <div class="container"> 
        <h1 style="text-align:center;color:green;"> 
            GeeksforGeeks 
        </h1> 

        <hr>

        <form> 
            <div class="form-group"> 
                <label for="">Enter Your Name:</label> 
                <input id="name" class="form-control"
                    type="text"
                    placeholder="Input Your Name Here"> 
            </div>

            <div class="form-group text-center"> 
                <button id="my_button"
                    class="btn btn-outline-success btn-lg"
                        type="button"> 
                    Add Name 
                </button> 
            </div> 
        </form> 

        <h3>List of Names:</h3>
        <div id="my_div"></div>
    </div> 

    <script>
        function append_to_div(div_name, data){
            document.getElementById(div_name).innerText += data;
        }

        document.getElementById("my_button")
                .addEventListener('click', function() {

            var user_name = document.getElementById("name");
            var value = user_name.value.trim();

            if(!value)
                alert("Name Cannot be empty!");
            else
                append_to_div("my_div", value+"\n");

            user_name.value = "";
        });
    </script>

</body> 

</html>
```

**输出:**

*   **Before adding data:**
    ![output_before](img/75a3a863b947e7c6f4ee34b275aeb648.png)
*   **After adding data:**
    ![output_after](img/8983a2639c112a6a32ec3a3f23e4967a.png)