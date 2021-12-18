# 如何用 JavaScript 将对象转换成字符串？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 将对象转换为字符串/](https://www.geeksforgeeks.org/how-to-convert-an-object-to-string-using-javascript/)

下面是将不同对象转换为字符串的方法。
**方法 1:使用函数 String()**
String()函数将对象的值转换为字符串。
**语法:**

```
String(object)
```

**参数:**

*   对象

**示例:**

```
<script> 
var bool_to_s1 = Boolean(0);
var bool_to_s2 = Boolean(1);
var num_to_s = 1234;

document.write( typeof( bool_to_s1)+"<br>");

document.write( typeof(String( bool_to_s1))+ "<br>");

document.write( typeof( bool_to_s2)+ "<br>"); 

document.write(typeof(String( bool_to_s2))+ "<br>"); 

document.write( typeof( num_to_s)+ "<br>"); 

document.write(typeof(String( num_to_s))+ "<br>"); 
</script>                    
```

**输出:**

```
boolean
string
boolean
string
number
string
```

**方法二:使用 JSON . stringify()**
JSON . stringify()将 javascript 对象转换为通过 web 服务器发送数据所需的字符串。

**语法:**

```
 JSON.stringify(obj)
```

**参数:**

*   可以是对象、数组

**示例:**

```
<script>
var obj_to_str = 
{ name: "GeeksForGeeks", city: "Noida", contact:2488 };
var myJSON = JSON.stringify(obj_to_str);
document.write(myJSON)
</script>
```

**输出:**

```
{"name":"GeeksForGeeks", "city":"Noida", "contact":2488}
```

更多关于 [JSON.stringify()](https://devdocs.io/javascript/global_objects/json/stringify)