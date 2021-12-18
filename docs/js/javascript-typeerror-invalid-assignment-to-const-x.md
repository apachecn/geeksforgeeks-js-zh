# JavaScript 类型错误–对常量“X”

的赋值无效

> 原文:[https://www . geesforgeks . org/JavaScript-type error-invalid-assignment-to-const-x/](https://www.geeksforgeeks.org/javascript-typeerror-invalid-assignment-to-const-x/)

如果用户试图更改常量值，就会出现这个 JavaScript 异常**对常量**的无效赋值。JavaScript 中的常量声明不能被重新赋值或重新声明。

**消息:**T0】

**错误类型:**

```
TypeError

```

**错误原因:**JavaScript 中的一个常量值被程序改变了，在正常执行过程中无法更改。

**示例 1:** 在本例中，变量(‘GFG’)的值发生了变化，因此出现了错误。

## HTML

```
<script>
    const GFG = "This is GFG";
    // Error here
    GFG = "This is GeeksForGeeks"; 
</script>
```

**输出(控制台):**

```
TypeError: Assignment to const

```

**示例 2:** 在本例中，对象(' GFG_Obj ')的值发生了变化，因此出现了错误。

## HTML

```
<script>
    const GFG_Obj = {key: 'val1'};
    // Error here
    GFG_Obj = {key: 'val2'}; 
</script>
```

**输出:**

```
TypeError: Assignment to const

```