# 如何用 JavaScript 在数组上同时使用映射和过滤？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 在数组上同时映射和过滤/](https://www.geeksforgeeks.org/how-to-use-map-and-filter-simultaneously-on-an-array-using-javascript/)

给定一个数组，任务是同时使用过滤器和映射函数到给定的数组。首先让我们简单地看一下映射和过滤函数:

*   **[filter() method:](https://www.geeksforgeeks.org/javascript-array-filter/)** This method returns a new array containing the elements that passes a certain test performed
    on an original array.

    **语法:**

    ```
    let newArray = oldArray.filter((currentValue, index, array) {
        // Returns element to new Array
    });

    ```

    **使用的参数和变量:**

    *   **新数组:**返回的数组。
    *   **旧数组:**过滤函数运行在这个数组的每个元素上。
    *   **当前值:**当前元素的值。
    *   **索引:**当前元素的数组索引..
    *   **数组:**当前元素所属的数组对象。
*   **[map() method:](https://www.geeksforgeeks.org/javascript-array-map-method/)** This method is used to apply a function on every element in an array and returns a new array of
    same size as the input array.

    **语法:**

    ```
    let newArray = oldArray.map((currentValue, index, array) {
        // Returns element to new Array
    });

    ```

    **使用的参数和变量:**

    *   **新数组:**要返回的数组。
    *   **旧数组:**映射函数运行在这个数组的每个元素上。
    *   **当前值:**当前元素的值。
    *   **索引:**当前元素的数组索引。
    *   **数组:**当前元素所属的数组对象。

**方法:**首先，通过使用 filter()函数，我们将从满足给定条件的数组中检索那些元素。因为 filter()方法将返回包含所需元素的数组。现在我们将应用 map()方法对 filter()方法返回的数组的所有元素执行指定的操作。

**示例:**

```
<script>
    /* Printing the name of students who play
       basketball using filter and map method 
       simultaneously. */

    // Taking an array of Student object
    let students = [
        { id: "001", name: "Anish", sports: "Cricket" },
        { id: "002", name: "Smriti", sports: "Basketball" },
        { id: "003", name: "Rahul", sports: "Cricket" },
        { id: "004", name: "Bakul", sports: "Basketball" },
        { id: "005", name: "Nikita", sports: "Hockey" }
    ]

    /* Applying filter function on students array to
       retrieve those students Objects who play 
       basketball and then the new array returned by
       filter method is mapped in order to get the name
       of basketball players instead of whole object.*/
    let basketballPlayers = students.filter(function (student) {
        return student.sports === "Basketball";
    }).map(function (student) {
        return student.name;
    })

    console.log("Basketball Players are:");

    // Printing out the name of Basketball players
    basketballPlayers.forEach(function (players) {
        console.log(players);
    });
</script>
```

**输出:**

```
Basketball Players are:
Smriti
Bakul

```