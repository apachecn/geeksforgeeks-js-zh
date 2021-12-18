# 用于的缺点..JavaScript 中的循环

> 原文:[https://www . geesforgeks . org/使用 for-in-in-loop-in-JavaScript 的缺点/](https://www.geeksforgeeks.org/disadvantages-of-using-for-in-loop-in-javascript/)

在本文中，我们将看到使用*的缺点是什么..在*循环中以及如何解决那些问题。

**用于的缺点..循环中:**

**原因 1:** 当你使用原型和任何其他数组在数组或对象中添加一个与该属性无关的属性时 **arr** 当你迭代数组 x 时，你得到了该属性。

**示例:**您在[**数组中添加了属性 *myCustomProp* 。**](https://www.geeksforgeeks.org/javascript-array-prototype-constructor/)

**语法:**

```
Array.prototype.myCustomProp = "Hello World";
```

现在创建一个数组 **x** 并给它赋值，然后遍历*进行..在*循环中。

## java 描述语言

```
<script>
  // Adding property using myCustomProp
  Array.prototype.myCustomProp = "Hello World";

  let arr = [1, 2, 3, 4, 5];

  // Iterating using for..in loop
  for (var index in arr) {
    console.log(arr[index]);
  }
</script>
```

**输出:**

```
1
2
3
4
5
"Hello World"
```

**解决方法:**你可以使用[*hasown property()*](https://www.geeksforgeeks.org/javascript-hasownproperty-method/)*的方法来解决这个问题。*

## *java 描述语言*

```
*<script>
  // Adding property using myCustomProp
  Array.prototype.myCustomProp = "Hello World";

  let arr = [1, 2, 3, 4, 5];

  // Iterating using for..in loop
  for (var index in arr) {
    // Checking if the item is present in arr or not
    if (arr.hasOwnProperty(index)) {
      console.log(arr[index]);
    }
  }
</script>*
```

***输出:***

```
*1
2
3
4
5*
```

***原因二:***为..在*循环中忽略数组的未定义值。假设你创建了一个空数组 **arr** 并给*arr【0】、arr【3】、arr【5】、* 分配了一些项目，这意味着*arr【1】、arr【2】、arr【4】*是*未定义的*，但是*为..在*循环中忽略它们。*

***示例:***

## *java 描述语言*

```
*<script>
  let arr = [];

  arr[0] = "A";
  arr[3] = "D";
  arr[5] = "F";

  console.log("Using for loop");

  for (var i = 0; i < arr.length; i++) {
    // "A", undefined, undefined, "D", undefined, "F"
    console.log(arr[i]);
  }

  console.log("Using for..in loop");

  for (var index in arr) {
    // "A", "D", "F"
    console.log(arr[index]);
  }
</script>*
```

***输出:***

*   ***用于循环:**

    ```
    "A"
    undefined
    undefined
    "D" 
    undefined
    "F"
    ```* 
*   ***用于..循环:**

    ```
    "A"
    "D"
    "F"
    ```* 

*一个简单的 *for* 循环打印数组的所有元素，包括*未定义*但*为..在*循环中忽略所有*未定义的*值。但是这是*真*仅适用于值未定义的数组，但是当*未定义的*明确存在于数组中时，则*适用于..在*循环中不忽略它们。*

## *java 描述语言*

```
*<script>
  let arr = [undefined, undefined, undefined, "Hello world"];

  for (var index in arr) {
    console.log(arr[index]);
  }
</script>*
```

***输出:***

```
*undefined
undefined
undefined
Hello World*
```