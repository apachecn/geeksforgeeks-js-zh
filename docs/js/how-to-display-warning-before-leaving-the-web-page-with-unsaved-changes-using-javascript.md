# 使用 JavaScript 离开有未保存更改的网页前如何显示警告？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 显示未保存更改的网页离开前警告/](https://www.geeksforgeeks.org/how-to-display-warning-before-leaving-the-web-page-with-unsaved-changes-using-javascript/)

**on beforenload**事件处理程序用于处理**beforenload**事件。每当窗口即将卸载其资源时，都会触发此事件。此事件的结果取决于用户选择继续还是取消操作。通过使用这种方法，此事件可用于检查用户是否留下了未完成或未保存的表单。

页面上的每个表单域都通过调用函数来更新各自的变量。每当触发卸载前的**时，都会检查这些变量，从而检查用户是否试图在不保存更改的情况下离开页面。如果表单是空的，它不会提醒用户，因为用户还没有开始填写表单。**

****语法:****

```html
// Event listener for the 'beforeunload' event
window.addEventListener('beforeunload', function (e) {

    // Check if any of the input fields are filled
    if (fname !== '' || lname !== '' || subject !== '') {

        // Cancel the event and show alert that
        // the unsaved changes would be lost
        e.preventDefault();
        e.returnValue = '';
    }
}); 
```

****示例:****

## **超文本标记语言**

```html
<!DOCTYPE html>
<html>

<head>
    <style>
        .container {
            border: 2px dotted;
            width: 60%;
            border-radius: 5px;
            padding: 10px;
        }

        input,
        textarea {
            width: 90%;
            padding: 10px;
            margin: 10px;
        }

        .submit-btn {
            background-color: green;
            color: white;
            padding: 10px;
        }
    </style>
</head>

<body>
    <h1 style="color: green;">
        GeeksforGeeks
    </h1>

    <p>
        The page will notify if the user has
        started filling the form and tries
        to navigate away from it.
    </p>

    <div class="container">
        <h2>A Demo Contact Form</h2>
        <form action="#">
            <label>First Name</label>

            <!-- Create all the input boxes and
            assign there respective functions
            to update the content in a variable -->
            <input type="text" id="fname" 
                name="firstname" 
                onchange="updateFname()">

            <label>Last Name</label>
            <input type="text" id="lname" 
                name="lastname" 
                onchange="updateLname()">

            <label>Subject</label>
            <textarea id="subject" name="subject" 
                style="height:100px" 
                onchange="updateSubject()">
        </textarea>

            <button class="submit-btn" 
                onclick="return false;">
                Submit
            </button>
        </form>
    </div>

    <script type="text/javascript">

        // Variables to store the input text
        let fname = '';
        let lname = '';
        let subject = '';

        // Functions to update the input text
        updateFname = () => {
            fname = document
                .getElementById('fname').value;
        }

        updateLname = () => {
            lname = document
                .getElementById('lname').value;
        }

        updateSubject = () => {
            subject = document
                .getElementById('subject').value;
        }

        // Event listener for the 
        // 'beforeunload' event
        window.addEventListener('beforeunload', 
                                function (e) {

            // Check if any of the input
            // fields are filled
            if (fname !== '' ||
                lname !== '' ||
                subject !== '') {

                // Cancel the event and
                // show alert that the unsaved
                // changes would be lost
                e.preventDefault();
                e.returnValue = '';
            }
        });
    </script>
</body>

</html>
```

****输出:****

**![](img/1e4fd1cd2c6f318adaedf955210926cc.png)**