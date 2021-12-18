# fabric . js resolvename espace()方法

> 原文:[https://www . geesforgeks . org/fabric-js-resolvenamespace-method/](https://www.geeksforgeeks.org/fabric-js-resolvenamespace-method/)

**resolveNamespace()方法**用于返回指定命名空间的对象。

**语法:**

```
resolveNamespace(namespace)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **命名空间:**此参数保存指定的命名空间字符串，例如“fabric”。Image.filter '，' fabric '等。

**返回值:**该方法返回指定命名空间的对象。

**例 1:**

## java 描述语言

```
<!DOCTYPE html>
<html>

<head>
  <!-- Adding the FabricJS library -->
  <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
  </script>
</head>

<body>
<script type="text/javascript">

  /* Calling resolveNamespace() function over
    the specified namespace */
  console.log(fabric.util.resolveNamespace("fabric.Observable"));
  console.log(fabric.util.resolveNamespace("fabric.util"));
</script>

</body>

</html>
```

**输出:**

```
{}
{"array":{},"object":{},"string":{},"ease":{}}
```

**例 2:**

## java 描述语言

```
<!DOCTYPE html>
<html>

<head>
  <!-- Adding the FabricJS library -->
  <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
  </script>
</head>

<body>
<script type="text/javascript">

   // Specifying some namespace
   var namespace1 = "fabric.CommonMethods";
   var namespace2 = "fabric.Collection";

  /* Calling resolveNamespace() function over
     the above specified namespace*/
  console.log(fabric.util.resolveNamespace(namespace1));
  console.log(fabric.util.resolveNamespace(namespace2));
</script>

</body>

</html>
```

**输出:**

```
{}
{"_objects":[]}
```