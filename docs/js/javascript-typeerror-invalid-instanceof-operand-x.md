# JavaScript type error–invalid ' instance of ' operators ' x '

> 哎哎哎:# t0]https://www . geeksforgeeks . org/JavaScript-type error-invalid-instance of-operators-x/

如果运算符的**实例的右操作数不能与构造函数对象一起使用，则会出现此 JavaScript 异常**无效的“实例”操作数**。它是一个包含原型属性的对象，可以被调用。**

**消息:**T0】

**错误类型:**

```
TypeError
```

**错误原因:****实例运算符**的右侧不是构造函数对象。

**例 1:** 在本例中，运算符右侧的**实例不是构造函数对象。**

## **HTML**

```
<script>
"Geeks" instanceof ""; // error here
</script>
```

**输出:**

```
TypeError: Right-hand side of 'instanceof' is not an object
```

**例 2:** 在本例中，运算符右侧的**实例不是构造函数对象。**

## **HTML**

```
<script>
function GFG() {}
var gfg = GFG();   
var x = new GFG();
x instanceof gfg; // error here
</script>
```

**输出:**

```
TypeError: Right-hand side of 'instanceof' is not an object
```