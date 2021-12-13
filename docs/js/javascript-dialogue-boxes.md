# JavaScript |对话框

> 原文:[https://www.geeksforgeeks.org/javascript-dialogue-boxes/](https://www.geeksforgeeks.org/javascript-dialogue-boxes/)

JavaScript 使用 3 种对话框: **ALERT** 、 **PROMPT** 和 **CONFIRM** 。这些对话框对于让我们的网站看起来更有吸引力非常有帮助。

### 警告框:

网站中使用了一个警告框，向用户显示警告消息，提示他们输入了错误的值，而不是需要填写的值。尽管如此，警告框仍然可以用于更友好的消息。警告框只给出一个按钮“确定”来选择和继续。

**例:**

## JavaScript

```html
<!DOCTYPE html>
<html>
   <head>

      <script</div>t type="text/javascript">
         <!--
            function Warning() {
               alert ("Warning danger you have not filled everything");
               document.write ("Warning danger you have not filled everything");
            }
      </script>

   </head>
   <body>

<p>Click me </p>

      <form>
         <input type="button" value="Click Me" onclick="Warning();" />
      </form>

   </body>
</html>
```