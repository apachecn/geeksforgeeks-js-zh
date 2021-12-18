# 内联 JavaScript 如何与 HTML 协同工作？

> 原文:[https://www . geesforgeks . org/how-do-inline-JavaScript-work-with-html/](https://www.geeksforgeeks.org/how-does-inline-javascript-work-with-html/)

内联 JavaScript 可以通过在 HTML 主体内部使用 **Script 标签**来实现，而不是在 Script 标签中指定 JavaScript 文件的来源(src =“…”)，我们必须**在 Script 标签**内部编写所有的 JavaScript 代码。

**语法:**

```
<script>
    // JavaScript Code
</script>

```

**示例:**

```
<!DOCTYPE html> 
<html> 

<head> 
    <title>Inline JavaScript</title> 
    <meta charset="utf-8"> 
    <meta name="viewport" 
          content="width=device-width, initial-scale=1"> 
    <link rel="stylesheet" 
          href= 
"https://maxcdn.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">
</head> 

<body> 
    <div class="container"> 
        <h1 style="text-align:center;color:green;"> 
          GeeksforGeeks 
      </h1> 
        <form> 
            <div class="form-group"> 
                <label for="">Enter Your Name:</label> 
                <input id="name"
                       class="form-control" 
                       type="text" 
                       placeholder="Input Your Name Here"> 
            </div> 
            <div class="form-group"> 
                <button id="btn-alert"
                        class="btn btn-success btn-lg float-right" 
                        type="submit"> 
                     Submit  
                </button> 
            </div> 
        </form> 
    </div> 
    <script>
        var user_name = document.getElementById("name");
        document.getElementById("btn-alert").addEventListener("click", function(){
            var value=user_name.value.trim();
            if(!value)
                alert("Name Cannot be empty!");
            else
                alert("Hello, " + value + "!\nGreetings From GeeksforGeeks.");
        });
    </script>
</body> 

</html> 
```

**输出:**

![inline_JS_output](img/7ec5fce94021660c846e85ebd87ec276.png)

只要我们输入一个名字并按下 submit 按钮，脚本标签内的 JavaScript 代码就会被触发，我们会得到一个带有我们的名字和问候文本的弹出消息。

![Inline_JS_Ouput_Popup](img/d76dd345f8599bee86a4677c0e02fc9a.png)

想了解更深层次的知识，可以访问[JavaScript 中的内联函数是什么？](https://www.geeksforgeeks.org/what-is-the-inline-function-in-javascript/)

**注意:**使用 Inline JavaScript 是一种不好的做法，不建议使用。它可以用于演示目的，因此演示者不必一次处理两个单独的文件。建议在单独的。然后在脚本标记中使用 src 属性链接相同的。