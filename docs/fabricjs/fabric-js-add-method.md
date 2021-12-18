# Fabric.js add()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-add-method/](https://www.geeksforgeeks.org/fabric-js-add-method/)

**add()方法**用于将一些指定的对象添加到新的集合中，并返回新创建的集合。

**语法:**

```
add(...object)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **对象:**此参数保存要添加到集合中的对象。

**返回值:**这个方法返回新创建的集合。

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

       // Calling add() function to add its
       // parameters into a collection of objects
       console.log(fabric.Collection.add(1, 2, 3));
       console.log(fabric.Collection.add("a", "b", "c"));
       console.log(fabric.Collection.add("gfg"));
   </script>

</body>

</html>
```

**输出:**

```
{"_objects":[1,2,3]}
{"_objects":[1,2,3,"a","b","c"]}
{"_objects":[1,2,3,"a","b","c","gfg"]}
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

       // Specifying some objects
       var obj1 = {name: "GFG"};
       var obj2 = {Department: "Computer Science"};
       console.log(fabric.Collection.add(obj1, obj2));
   </script>

</body>

</html>
```

**输出:**

```
{"_objects":[{"name":"GFG"},{"Department":"Computer Science"}]}
```