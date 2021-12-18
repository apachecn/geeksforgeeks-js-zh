# 声明 JavaScript 数组时“Array()”和“[]”有什么区别？

> 原文:[https://www . geesforgeks . org/数组和声明一个 javascript 数组的区别是什么/](https://www.geeksforgeeks.org/whats-the-difference-between-array-and-while-declaring-a-javascript-array/)

**考虑以下代码:**

```
var myArray = new Array(5);
```

和

```
var myArray = [5];
```

虽然这两行可能看起来相同，但事实并非如此。

**考虑以下解释:**
**情况 1: var myArray = new Array(5)**

*   This method is used to define an array of length 5\. The parameter passed here ‘5’ is an argument that defines the initial length of the array to be made. Hence any value can be passed to get the array of that length using this code.

    ```
    // Write Javascript code here
    //Creates an array of 5 undefined elements 
    var arr = new Array(5); 

    alert(arr.length);
    ```

    **输出:**

    ```
    5

    ```

*   使用此方法的另一个优点是，它会在堆栈中预先创建所需的数组大小。这反过来有助于避免 StackOverflow 错误。

**情况 2: var myArray = [5]**

*   This method is used to define an array of with the values where the length of the array is equal to the number of values passed to in the square brackets. The parameter passed here ‘5’ is the value for myArray’s 0th element, i.e. myArray[0] = 5.

    ```
    // Write Javascript code here
    //Creates an array of 5 undefined elements 
    var arr = [5]; 

    alert(arr[0]);
    alert("\n"+arr.length);
    ```

    **输出:**

    ```
    5
    1

    ```

*   此方法不会预先在堆栈中创建所需大小的数组。因此，该方法需要在每次数组扩展时定义内存，这又会导致堆栈溢出错误。