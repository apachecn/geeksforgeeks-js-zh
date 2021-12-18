# 如何用 JavaScript 映射、缩小、过滤一个 Set 元素？

> 原文:[https://www . geeksforgeeks . org/如何使用 javascript 映射、减少和过滤集合元素/](https://www.geeksforgeeks.org/how-to-map-reduce-and-filter-a-set-element-using-javascript/)

map()，reduce()和 filter()是数组函数，它们根据应用的函数转换数组并返回更新的数组。它们用于编写简单、简短和干净的代码来修改数组，而不是使用循环。

*   **[map() method:](https://www.geeksforgeeks.org/javascript-array-map-method/)** It applies a given function on all the elements of the array and returns the updated array. It is the simpler and shorter code instead of a loop. The map is similar to the following code:

    ```
    arr = new Array(1, 2, 3, 6, 5, 4);
    for(int i = 0; i < 6; i++) {
        arr[i] *= 3;
    }
    ```

    **语法:**

    ```
    array.map(*function_to_be_applied*)
    ```

    ```
    array.map(function (*args*) {
        // code;
    })

    ```

    **示例:**

    ```
    function triple(n){
        return n*3;
    }    
    arr = new Array(1, 2, 3, 6, 5, 4);

    var new_arr = arr.map(triple)
    console.log(new_arr);
    ```

    ```
    Output: 
    [ 3, 6, 9, 18, 15, 12 ]

    ```

*   **[reduce() method:](https://www.geeksforgeeks.org/javascript-array-reduce-method/)** It reduces all the elements of the array to a single value by repeatedly applying a function. It is an alternative of using a loop and updating the result for every scanned element. Reduce can be used in place of the following code:

    ```
    arr = new Array(1, 2, 3, 6, 5, 4);
    result = 1
    for(int i = 0; i < 6; i++) {
        result = result * arr[i];
    }
    ```

    **语法:**

    ```
    array.reduce(*function_to_be_applied*)
    ```

    ```
    array.reduce(function (*args*) {
        // code;
    })

    ```

    **示例:**

    ```
    function product(a, b){
        return a * b;
    }
    arr = new Array(1, 2, 3, 6, 5, 4);

    var product_of_arr = arr.reduce(product)
    console.log(product_of_arr)
    ```

    **输出:**

    ```
    720
    ```

*   **[filter() method:](https://www.geeksforgeeks.org/javascript-array-filter/)** It filters the elements of the array that return false for the applied condition and returns the array which contains elements that satisfy the applied condition. It is a simpler and shorter code instead of the below code using a loop:

    ```
    arr = new Array(1, 2, 3, 6, 5, 4);
    new_arr = {}
    for(int i = 0; i < 6; i++) {
        if(arr[i] % 2 == 0) {
             new_arr.push(arr[i]);           
        }
    }
    ```

    **语法:**

    ```
    array.filter(*function_to_be_applied*)
    ```

    ```
    array.filter(function (*args*) {
        // condition;
    })

    ```

    **示例:**

    ```
    arr = new Array(1, 2, 3, 6, 5, 4);
    var new_arr = arr.filter(function (x){
        return x % 2==0;
    });

    console.log(new_arr)
    ```

    **输出:**

    ```
    [ 2, 6, 4 ]
    ```