# JavaScript 字符串 lastIndexOf()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-prototype-last indexof-function/](https://www.geeksforgeeks.org/javascript-string-prototype-lastindexof-function/)

下面是 String lastIndexOf()方法的示例。

*   **例:**

    ```
    <script> 
    function func() { 
        var str = 'GeeksforGeeks'; 
        var index = str.lastIndexOf('for'); 
        document.write(index); 
    } 
    func(); 
    </script>
    ```

*   输出:

    ```
    5

    ```

**str.lastIndexOf()** 方法查找给定字符串中参数字符串最后一次出现的索引。返回值从 0 开始。

**语法:**

```
str.lastIndexOf(searchValue , index)

```

**Perameters:**

*   **搜索值:**搜索值是要在基本字符串中搜索的字符串。*   **index** defines the starting index from where the **searchValue** is to be searched in the base string backwards.

    **返回值:**该方法返回最后一次找到**搜索值**的字符串的索引(从 0 开始)。如果在字符串中找不到**搜索值**，则该方法返回 **-1** 。

    <u>*上述方法示例如下:*</u>

    **例 1:**

    ```
    var str = 'Departed Train';
    var index = str.lastIndexOf('Train');
    print(index); 

    ```

    输出:

    ```
    9

    ```

    在本例中，方法 **lastIndexOf()** 在字符串**字符串**中找到字符串**“列车”**的最后一个索引。由于字符串的唯一索引是 9，因此该方法返回 **9** 作为答案。

    **例 2:**

    ```
    var str = 'Departed Train';
    var index = str.lastIndexOf('ed Tr');
    print(index); 

    ```

    输出:

    ```
    6

    ```

    在本例中，方法 **lastIndexOf()** 在字符串**字符串**中找到字符串**的最后一个索引**。由于该字符串所在位置的唯一索引是 6，因此该方法返回 **6** 作为答案。

    **例 3:**

    ```
    print('Departed Train'.lastIndexOf('train')); 

    ```

    输出:

    ```
    -1

    ```

    在本例中，方法 **lastIndexOf()** 在字符串**字符串**中找到字符串**“火车”**的最后一个索引。由于该字符串不存在于**字符串**的任何索引中，因此该方法返回 **-1** 作为答案。

    **例 4:**

    ```
    print('Departed Train before another Train'.lastIndexOf('Train')); ; 

    ```

    输出:

    ```
    6

    ```

    在本例中，方法 **lastIndexOf()** 找到字符串 **Train** 在字符串 **str** 中的最后一个索引。由于字符串在字符串**字符串**和索引 **30** 中出现两次，是**列车**的最后一个索引，因此该方法返回 **30** 作为答案。

    <u>*上述方法的代码如下:*</u>

    **程序 1:**

    ```
    <script>
    // JavaScript to illustrate lastIndexOf() method

    function func() {

        //Original string
        var str = 'Departed Train';

        //Finding the index of the string
        var index = str.lastIndexOf('Train');
        document.write(index);
    }
    func();
    </script>
    ```

    输出:

    ```
    9

    ```

    **程序 2:**

    ```
    <script>
    // JavaScript to illustrate lastIndexOf() method

    function func() {

        // Original string
        var str = 'Departed Train';

        // Finding the index of the string
        var index = str.lastIndexOf('ed Tr');
        document.write(index); 
    }
    func();
    </script> 
    ```

    输出:

    ```
    6

    ```

    **程序 3:**

    ```
    <script>
    // JavaScript to illustrate lastIndexOf() method

    function func() {

        // Original string
        var str = 'Departed Train';

        // Finding index of occurrence of 'train'
        var index = str.lastIndexOf('train');
        document.write(index);
    }
    func();
    </script>
    ```

    输出:

    ```
    -1

    ```

    **程序 4:**

    ```
    <script>
    // JavaScript to illustrate lastIndexOf() method

    function func() {

        // Original string
        var str = 'Departed Train before another Train';

        // Finding index of occurrence of 'Train'
        var index = str.lastIndexOf('Train');
        document.write(index); ;
    }
    func();
    </script>
    ```

    输出:

    ```
    30

    ```

    **支持的浏览器:**

    *   Chrome 1 及以上
    *   边缘 12 及以上
    *   Firefox 1 及以上版本
    *   Internet Explorer 6 及以上版本
    *   歌剧 3 及以上
    *   Safari 1 及以上