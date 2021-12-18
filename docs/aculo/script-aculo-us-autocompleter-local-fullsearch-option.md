# script.aculo.us 自动完成器。本地完整搜索选项

> 原文:[https://www . geesforgeks . org/script-aculo-us-autocompleter-local-full search-option/](https://www.geeksforgeeks.org/script-aculo-us-autocompleter-local-fullsearch-option/)

script.aculo.us 库是一个跨浏览器库，旨在改善网站的用户界面。自动完成器可用于为网页中的文本字段提供自动完成支持。当自动完成选项作为自动完成方法的数组提供给选项显示时，使用本地自动完成器。

**自动完成器。本地全搜索** 选项是用来指定自动完成器是只在字符串的开头匹配输入的文本，还是匹配给定数组中的所有字符。

**语法:**

```
{ fullSearch: boolean }

```

**值:**

*   **布尔值:**这是一个布尔值，指定文本是否匹配字符串中的任何位置。默认值为假。

**示例 1:** 在本例中，我们将 fullSearch 选项设置为 false，因此它不会从字符串中的任何位置进行搜索。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <!-- Include the required scripts -->
    <script type="text/javascript" 
        src="prototype.js">
    </script>

    <script type="text/javascript" 
src="scriptaculous.js?load = effects,controls">
    </script>
</head>

<body>
    <h1>GeeksforGeeks</h1>

    <label for="GeeksforGeeks">
        Input any name:
    </label>

    <br />
    <input id="GeeksforGeeks" autocomplete="off"
        size="40" type="text" value="" />

    <div class="autocomplete" id="names" 
        style="display:none">
    </div>

    <script type="text/javascript">

        // Array to be used as choices
        var names = [
            'Ab',
            'Abc',
            'Abcd',
            'Abcde',
            'Abcdef',
            'Abcdefg',
            'Abcdefgh'
        ];

        // Initialize the Autocompleter
        new Autocompleter.Local('GeeksforGeeks',
            'names', names, {

            // Specify whether the strings would
            // be searched at all positions
            fullSearch: false
        });
    </script>
</body>

</html>
```

**输出:**

![](img/d0cc01de363a37624816e0c18fa0fc33.png)

**示例 2:** 在本例中，我们必须将 fullSearch 选项设置为 true，因此它可以从字符串中的任何位置进行搜索。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <!-- Include the required scripts -->
    <script type="text/javascript" 
        src="prototype.js">
    </script>

    <script type="text/javascript" 
src="scriptaculous.js?load = effects,controls">
    </script>
</head>

<body>
    <h1>GeeksforGeeks</h1>

    <label for="GeeksforGeeks">
        Input any name:
    </label>

    <br />
    <input id="GeeksforGeeks" autocomplete="off" 
        size="40" type="text" value="" />

    <div class="autocomplete" id="names" 
        style="display:none">
    </div>

    <script type="text/javascript">

        // Array to be used as choices
        var names = [
            'Ab',
            'Abc',
            'Abcd',
            'Abcde',
            'Abcdef',
            'Abcdefg',
            'Abcdefgh'
        ];

        // Initialize the Autocompleter
        new Autocompleter.Local('GeeksforGeeks',
            'names', names, {

            // Specify whether the strings would
            // be searched at all positions
            fullSearch: true
        });
    </script>
</body>

</html>
```

**输出:**

![](img/e8a5bf4db953ef9c15fca5e62f575173.png)