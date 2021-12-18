# fabric . js graph mesplit()方法

> 原文:[https://www . geesforgeks . org/fabric-js-graph mesplit-method/](https://www.geeksforgeeks.org/fabric-js-graphemesplit-method/)

**graph mesplit()方法**用于将指定的字符串以用户感知的单个单位划分，即指定字符串的每个字符将被转换为单个字符串单位。

**语法:**

```
graphemeSplit(textstring)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **textstring:** 此参数保存要划分的字符串。

**返回值:**该方法返回包含被划分字符的字形的数组。

**例 1:**

## java 描述语言

```
<!DOCTYPE html>

<html>

<head>
   <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js" >
   </script>

   <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js.map">
   </script>

   <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.js">
   </script>
</head>

<body>
   <script type="text/javascript">
        console.log(fabric.util.string.graphemeSplit("GFG"));
        console.log(fabric.util.string.graphemeSplit("G F G"));
   </script>

</body>

</html>
```

**输出:**

```
["G","F","G"]
["G"," ","F"," ","G"]
```

**例 2:**

## java 描述语言

```
<!DOCTYPE html>

<html>

<head>
   <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js" >
   </script>

   <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js.map">
   </script>

   <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.js">
   </script>
</head>

<body>
   <script type="text/javascript">
       console.log("Using graphemeSplit() Function:");
       var value = "12ab";
       console.log(fabric.util.string.graphemeSplit(value));

       console.log("Without using graphemeSplit() Function:");
       var value="12ab";
       console.log(value);
   </script>

</body>

</html>
```

**输出:**

```
Using graphemeSplit() Function:
["1","2","a","b"]
Without using graphemeSplit() Function:
12ab
```