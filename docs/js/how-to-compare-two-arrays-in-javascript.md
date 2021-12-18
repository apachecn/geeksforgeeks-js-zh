# 如何在 JavaScript 中比较两个数组？

> 原文:[https://www . geesforgeks . org/如何比较 javascript 中的两个数组/](https://www.geeksforgeeks.org/how-to-compare-two-arrays-in-javascript/)

在本文中，任务是比较两个数组，&我们需要检查两个数组的长度应该是相同的，它们中存在的对象是相同的类型，并且一个数组中的每一项都等于另一个数组中的对应项。通过这样做，我们可以得出两个数组是否相同的结论。JavaScript 提供了一个函数 [**JSON.stringify()**](https://www.geeksforgeeks.org/javascript-json-stringify-method/) 方法，以便将对象或数组转换为 JSON 字符串。通过转换成 JSON 字符串，我们可以直接检查字符串是否相等。

**示例 1:** 本示例使用 **JSON.stringify()** 方法将对象或数组转换为 JSON 字符串，然后相应地检查给定的条件。如果它满足特定条件，则返回真，否则返回假。

## Javascript

```
<script>
  var a = [1, 2, 3, 5];
  var b = [1, 2, 3, 5];

  // Comparing both arrays using stringify
  if(JSON.stringify(a)==JSON.stringify(b))
   document.write("True");
  else
   document.write("False");
   document.write('<br>');
  var f=[1, 2, 4, 5];
  if(JSON.stringify(a)==JSON.stringify(f))
   document.write("True");
  else
   document.write("False");
</script>
```

**输出:**

```
True
False
```

**例 2:** 在本例中，我们手动检查每一个项目，如果它们相等，则返回*真*，否则返回*假*。

## Javascript

```
<script>
  function isEqual()
  {
   var a = [1, 2, 3, 5];
   var b = [1, 2, 3, 5];

    // If length is not equal
    if(a.length!=b.length)
     return "False";
    else
    {

    // Comparing each element of array
     for(var i=0;i<a.length;i++)
     if(a[i]!=b[i])
      return "False";
      return "True";
    }
  }
  var v = isEqual();
  document.write(v);
</script>
```

**输出:**

```
True
```

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。