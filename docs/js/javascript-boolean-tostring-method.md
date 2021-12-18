# JavaScript 布尔 toString()方法

> 原文:[https://www . geesforgeks . org/JavaScript-boolean-tostring-method/](https://www.geeksforgeeks.org/javascript-boolean-tostring-method/)

下面是**布尔 toString()** 方法的例子。

*   **例:**

    ```
    <script>
      // Here Boolean object obj 
      // is created for the value 27
      var obj = new Boolean(27);

      // Here boolean.toString() function is 
      // used for the created object obj.
      document.write(obj.toString());
    </script>
    ```

*   **输出:**

    ```
    true
    ```

**boolean.toString()** 方法用于根据指定布尔对象的值返回字符串“ **true** 或“ **false** ”。

**语法:**

```
boolean.toString()
```

**参数:**此方法不接受任何参数。
**返回值:**根据指定布尔对象的值，返回一个字符串“真”或“假”。

上述方法的更多代码如下:

*   **Example 1:**

    ```
    <script>
      // Here Boolean object obj is 
      // created for the value true.
      var obj = new Boolean(true);

      // Here boolean.toString() function
      // is used for the created object obj.
      document.write(obj.toString());
    </script>
    ```

    **输出:**

    ```
    true
    ```

*   **Example 2:**

    ```
    <script>
      // Here Boolean object obj is 
      // created for the value 1.
      var obj = new Boolean(1);

      // Here boolean.toString() function is
      // used for the created object obj.
      document.write(obj.toString());
    </script>
    ```

    **输出:**

    ```
    true
    ```

*   **Example 3:**

    ```
    <script>
      // Here Boolean object obj is
      // created for the value -1.
      var obj = new Boolean(-1);

      // Here boolean.toString() function is
      // used for the created object obj.
      document.write(obj.toString());
    </script>
    ```

    **输出:**

    ```
    true
    ```

*   **Example 4:**

    ```
    <script>
      // Here Boolean object obj is
      // created for the value 1.2
      var obj = new Boolean(1.2);

      // Here boolean.toString() function is
      // used for the created object obj.
      document.write(obj.toString());
    </script>
    ```

    **输出:**

    ```
    true
    ```

*   **Example 5:**

    ```
    <script>
      // Here Boolean object obj is created 
      // for the value as string "gfg"
      var obj = new Boolean("gfg");

      // Here boolean.toString() function is 
      // used for the created object obj.
      document.write(obj.toString());
    </script>
    ```

    **输出:**

    ```
    true
    ```

*   **Example 6:**

    ```
    <script>
      // Here Boolean object obj is created
      // for the value false.
      var obj = new Boolean(false);

      // Here boolean.toString() function is
      // used for the created object obj.
      document.write(obj.toString());
    </script>
    ```

    **输出:**

    ```
    false
    ```

**错误和异常:**

*   **Example 1:** Here the value as geeksforgeeks gives error because this value is not defined only true and false has been predefined.

    ```
    <script>
      // Here Boolean object obj is created 
      // for the value geeksforgeeks.
      var obj = new Boolean(geeksforgeeks);

      // Here boolean.toString() function is
      // used for the created object obj.
      console.log(obj.toString());
    </script>
    ```

    **输出:**

    ```
    Error: geeksforgeeks is not defined
    ```

*   **Example 2:** Here complex number can not be taken as the parameter only integer values and string can be taken as the parameter that is why it returns error.

    ```
    <script>
      // Here Boolean object obj is created for the
      // value such as complex number 1+2i
      var obj = new Boolean(1 + 2i);

      // Here boolean.toString() function is 
      // used for the created object obj.
      console.log(obj.toString());
    </script>
    ```

    **输出:**

    ```
    Error: Invalid or unexpected token
    ```

**支持的浏览器:**JavaScript Boolean toString()方法支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   Mozilla Firefox
*   旅行队
*   歌剧