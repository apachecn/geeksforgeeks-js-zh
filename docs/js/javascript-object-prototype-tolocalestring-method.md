# JavaScript object . prototype . ToLocalString()方法

> 原文:[https://www . geesforgeks . org/JavaScript-object-prototype-tolocalesting-method/](https://www.geeksforgeeks.org/javascript-object-prototype-tolocalestring-method/)

方法使用环境的区域设置返回这个对象的本地特定字符串表示。像[数组](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwi-_JaYgpLwAhWm63MBHWWJDmwQFjABegQIBRAD&url=https%3A%2F%2Fwww.geeksforgeeks.org%2Farrays-in-javascript%2F&usg=AOvVaw39mcwW1ycx6JqMqAM5hfFZ)、数字、日期、 [typedarray](https://www.geeksforgeeks.org/typedarray-introduction/) 和 [BigInt](https://www.geeksforgeeks.org/bigint-in-javascript/) 这样的派生对象可以覆盖此方法。

**语法:**

```
object.toLocaleString()
```

**返回值:**返回该对象的字符串表示形式。

**对象覆盖 ToLocalString():**

**1。array to**[**array . prototype . tolocalestring()**](https://www.geeksforgeeks.org/javascript-array-tolocalestring-function/)**:**它返回这个数组对象的字符串表示。

**例:**

## Javascript

```
// User inputs.
var name = [ "sahil", "zain", "deepanshu" ];
var number1 = 3.45;
var number2 = [ 23, 34, 54 ];

var arr = [ name, number1, number2 ];

// Applying array.toLocaleString function
var string = arr.toLocaleString();

// Printing string.
console.log(string);
```

**输出:**

```
"sahil, zain, deepanshu, 3.45, 23, 34, 54"
```

**2。BigInt to**[**BigInt . prototype . tolocalesting()**](https://www.geeksforgeeks.org/javascript-bigint-prototype-tolocalestring-method/)**:**它返回这个 BigInt 对象的字符串表示形式。

**例:**

## Javascript

```
var Big = 45334n;
console.log(Big.toLocaleString());

Big =78753456789123456789n;
console.log(Big.toLocaleString('de-DE'));
```