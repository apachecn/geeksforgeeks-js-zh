# 如何使用 JavaScript 验证确认密码？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 验证-确认-密码/](https://www.geeksforgeeks.org/how-to-validate-confirm-password-using-javascript/)

几乎在每一个现代网站上，我们都看到了登录和注册功能，这对客户和服务提供商来说都是一项重要的服务。当用户注册某个网站时，他们必须输入用户名和密码，为了输入密码，网站要求他们输入两次密码，这是为了用户的安全，即输入的密码是否相同。在这篇文章中。我们将使用 [HTML](https://www.geeksforgeeks.org/html-tutorials/) 、 [CSS](https://www.geeksforgeeks.org/css-tutorials/) 和 [javascript](https://www.geeksforgeeks.org/javascript-tutorial/) 创建一个确认密码验证。

**方法:**我们将制作一个简单的登录卡，其中将有三个输入，一个是用户名，可以是本文的任何内容，第二个是密码，第三个输入是确认密码。首先，我们将在密码输入和确认密码输入中键入密码，然后我们将比较两个输入是否相同，如果输入相同，我们将在确认密码输入框下方显示“密码匹配”，如果输入不相同，我们将显示红色的“使用相同的密码”，以便用户键入相同的密码。

下面是上述方法的实现。

## 超文本标记语言

```
<!DOCTYPE html>

<head>
    <title>Confirm Password validation using javascript</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: rgb(50, 57, 78);
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .main {

            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            background-color: rgb(34, 34, 34);
            height: 400px;
            width: 300px;
            margin-top: 15%;
            border-radius: 10px;
            box-shadow: 2px 4px 6px rgb(0, 0, 0);
        }

        .pass {
            display: flex;
            flex-direction: column;
        }

        .image h2 {
            color: rgb(2, 149, 27);
            font-size: 30px;
            font-family: sans-serif;
            margin-bottom: 50px;
        }

        .username input,
        .pass input {
            font-family: sans-serif;
            margin-bottom: 20px;
            height: 30px;
            border-radius: 100px;
            border: none;
            text-align: center;
            outline: none;
        }

        .submit_btn {
            height: 30px;
            width: 80px;
            border-radius: 100px;
            border: none;
            outline: none;
            background-color: rgb(0, 179, 95);
            margin-top: 15px;
        }

        .submit_btn:hover {
            background-color: rgba(0, 179, 95, 0.596);
            color: rgb(14, 14, 14);
            cursor: pointer;
        }
    </style>
</head>

<body>
    <div class="main">
        <div class="image">
            <h2>GeeksforGeeks</h2>
        </div>
        <div class="username">
            <input type="text" 
                   name="username" 
                   placeholder="Dummyuser">
        </div>
        <div class="pass">
            <input id="pass" 
                   type="password" 
                   name="pass" 
                   placeholder="Enter Password" 
                   required"">
            <input id="confirm_pass" 
                   type="password" 
                   name="confirm_pass" 
                   placeholder="Confirm Password" 
                   required
                   onkeyup="validate_password()">
        </div>
        <span id="wrong_pass_alert"></span>
        <div class="buttons">
            <button id="create" 
                    class="submit_btn" 
                    onclick="wrong_pass_alert()">
                Submit
            </button>
        </div>
    </div>
    <script>
        function validate_password() {

            var pass = document.getElementById('pass').value;
            var confirm_pass = document.getElementById('confirm_pass').value;
            if (pass != confirm_pass) {
                document.getElementById('wrong_pass_alert').style.color = 'red';
                document.getElementById('wrong_pass_alert').innerHTML 
                  = '☒ Use same password';
                document.getElementById('create').disabled = true;
                document.getElementById('create').style.opacity = (0.4);
            } else {
                document.getElementById('wrong_pass_alert').style.color = 'green';
                document.getElementById('wrong_pass_alert').innerHTML =
                    '🗹 Password Matched';
                document.getElementById('create').disabled = false;
                document.getElementById('create').style.opacity = (1);
            }
        }

        function wrong_pass_alert() {
            if (document.getElementById('pass').value != "" &&
                document.getElementById('confirm_pass').value != "") {
                alert("Your responce is submitted");
            } else {
                alert("Please fill all the fields");
            }
        }
    </script>
</body>

</html>
```

**输出:** ![](img/9a2c9b333f2b356d33cdd3d7baa6930d.png)