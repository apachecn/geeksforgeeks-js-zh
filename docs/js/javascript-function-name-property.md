# JavaScript 函数名属性

> 原文:[https://www . geesforgeks . org/JavaScript-function-name-property/](https://www.geeksforgeeks.org/javascript-function-name-property/)

下面是**函数名属性的一个基本例子。**

*   **示例:**

## java 描述语言

```
<script>
  // Creating function name func1
  function func1(){
  }
  document.write(func1.name)
</script>
```

*   **输出:**

```
func1

```

javascript 对象的**函数名**属性用于返回函数名。函数的这个 name 属性只能读取，不能更改。创建函数时给定的函数名由函数名返回

**语法:**

```
Function.name

```

**属性值:**该属性有如下三个属性:

*   **可写:**否
*   **可读:**否
*   **可配置:**是

**返回:**该属性返回字符串，即函数的名称。

下面提供了上述属性的代码:

**程序 1:** 给出简单函数时

## 超文本标记语言

```
<script>
    // Creating function name func1
    function func1(){
    }
    // Creating function name func2
    function func2(a,b){
    }
    document.write("Name of the function func2 is: "
    ,func1.name +"<br>")
    document.write("Name of the function func2 is: "
    ,func2.name +"<br>")

    // Logging return type to console
    document.write("Type of func.name is: "
    ,typeof(func2.name))
</script>
```

**输出:**

```
Name of the function func2 is: func1
Name of the function func2 is: func2
Type of func.name is: string
```

**程序 2:** 当给定一个功能对象时。

## 超文本标记语言

```
<script>
    // Creating object of functions
    let obj={
      function1:function functionName1(){},

      function2:()=>{
        console.log("function2 is running")
      },
      function3:()=>{
        obj.function2();
      },
    }
    obj.function3()
    // Calling object function1 but function 
    // name is functionName1
    document.write("Name of the function function1 is: "
                ,obj.function1.name+"<br>")
    document.write("Name of the function function3 is: "
                ,obj.function3.name+"<br>")
</script>
```

**输出:**

```
Name of the function function1 is: functionName1
Name of the function function3 is: function3
```

**程序 3:** 在函数实例上使用 name 属性。

## 超文本标记语言

```
<script>
    // Function func
    function func() {};
    // Obj is the instance of the 
    // function object func
    let obj = new func();
    if (obj.constructor.name === "func")
      document.write("obj",obj,
      "is an instance of function func")
    else
      document.write('Oops!')
</script>
```

**输出:**

```
obj[object Object]is an instance of function func
```

**程序 4:** 使用有界函数上的 name 属性。

## 超文本标记语言

```
<script>
    // Function func
    function func() {};
    // Logging bounded function to console.
    document.write("Name of the bounded func is: "
    ,func.bind({}).name)
  </script>
```

**输出:**

```
Name of the bounded func is: bound func
```

**支持的浏览器:**

*   谷歌 Chrome 15 及以上版本
*   Firefox 1 及以上版本
*   Safari 6 及以上版本
*   微软 Edge 14 及以上版本
*   Opera 10.5 及以上