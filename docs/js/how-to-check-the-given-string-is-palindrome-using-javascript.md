# 如何用 JavaScript 检查给定的字符串是回文？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 检查给定字符串是否是回文/](https://www.geeksforgeeks.org/how-to-check-the-given-string-is-palindrome-using-javascript/)

A **回文**是一个从后往前读都一样的单词、句子或偶数。因此，如果我们接受输入，反转字符串并检查反转后的字符串和原始字符串是否相等，这意味着该字符串是回文，否则不是。

**进场:**

1.  When users click the submit button, we run a JavaScript function.
2.  Let's convert the string to lowercase first.
3.  Then we use **split () method** to divide the string into an array, so that we can use **reverse () method** to reverse it.
4.  Then we use the **join () method to connect the array back to the string.**
5.  Finally, we check whether the input string and the inverted string are equal. We will update the output accordingly.

**例:**

```html
<!DOCTYPE html>
<html>

<head>
    <style>
        body {
            background-color: grey;
        }

        .container {
            background-color: #00ffff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 60vh;
            width: 80vw;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            border-radius: 25px;
            box-shadow: 2px 31px 35px -15px
                        rgba(0, 0, 0, 0.1);
            padding: 10px;
        }

        .pallindrome {
            width: 500px;
        }

        .input-container {
            text-align: center;
            margin: 30px 0;

        }

        .btn-container {
            text-align: center;
        }

        input {
            width: 70%;
            border: none;
            padding: 15px;
            font-size: 1.1rem;
            border-radius: 10px;
        }
    </style>

</head>

<body>
    <div class="container">
        <div class="pallindrome">
            <header>
                <h1>Palindrome checking using
                    CSS and JavaScript</h1>
            </header>
            <div class="main">
                <div class="input-container">

                    <!-- Place to input the string -->
                    <input type="text" placeholder="Enter...">
                </div>
                <div class="btn-container">

                    <!-- Button that will activate the check  -->
                    <button>Check</button>
                </div>
                <div>
                    <b>Input String: </b>
                    <span class="input-string"></span>
                    <br>
                    <b>Reversed String: </b>
                    <span class="reversed-string"></span>
                    <p class="output-text"></p>

                </div>
            </div>
        </div>
    </div>
    <script src="script.js"></script>
</body>

</html>
```