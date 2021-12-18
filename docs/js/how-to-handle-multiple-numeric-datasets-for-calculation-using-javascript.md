# 如何使用 JavaScript 处理多个数值数据集进行计算？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 处理用于计算的多数值数据集/](https://www.geeksforgeeks.org/how-to-handle-multiple-numeric-datasets-for-calculation-using-javascript/)

假设我们已经给定了一个由多个**数值**组成的数据集，任务是使用该数据集进行一些计算。因此，我们将使用对象数组创建**字典**这样的数据结构。我们将讨论如何使用一些 JavaScript 方法来处理这种类型的数据。为了处理多个数值数据集进行计算，我们可以使用 JavaScript[**filter()**](https://www.geeksforgeeks.org/javascript-array-filter/)函数和 [**find()**](https://www.geeksforgeeks.org/javascript-array-find-method/) 函数。

**举例:**给定一个员工数据。

```
 id |age |  sal  | exp | com
344 | 45 | 40000 | 12  |  3000
672 | 32 | 30000 | 5   |  8000
```

我们必须遵循几个步骤在多个数据集上执行计算。

**注意:**对象数组允许您在单个变量中存储多个值。它存储相同类型元素的固定大小的顺序集合。因此，我们在这里使用了一个类似字典的对象数组。

**步骤 1:** 我们将这个数据集转换成如下所示的对象数组:

```
// Array of the dictionary object
employee = [
    {id: 344, age: 45, sal: 40000, exp: 12, com: 3000},
    {id: 672, age: 32, sal: 30000, exp: 5, com: 8000}
]
```

**步骤 2:** 现在我们已经有了对象数组形式的数据集。

*   **示例 1:** 现在我们将了解如何根据我们的需要来操作或处理数据。在本例中使用 [**过滤器()**](https://www.geeksforgeeks.org/javascript-array-filter/) 方法(可以计算多个值。)

    ```

    <script>

        // Array of the dictionary object
        employee = [{
                id: 344,
                age: 45,
                sal: 40000,
                exp: 12,
                com: 3000
            },
            {
                id: 672,
                age: 32,
                sal: 30000,
                exp: 5,
                com: 8000
            }
        ]

    /* Method that calculates the total salary 
    of the employees according to the given
    experience*/
    function totalIncome(exp) {

        /* The filter() method uses another conditional
        method as an argument */
        let empWithExp = employee.filter((emp) => emp.exp === exp);
        let result = 0;

        /* All the employee's total salary with given experience is
        calculated here we are using forEach() method to calculate 
        salary of more than one employees */
        empWithExp.forEach((emp) => {
            result += emp.sal + emp.com;
        });
        return result;
    }
    //printing and calling the method totalIncome()
    document.write("Total income of Employee with experience "+
                " of 12years: " + totalIncome(12)); 
    </script>                    
    ```

*   **输出:**

    ```
    Total income of Employee with experience of 12years: 43000
    ```

*   **示例 2:** 在本例中使用 [**find()**](https://www.geeksforgeeks.org/javascript-array-find-method/) 方法(仅用于计算 id 等唯一数据的值)。

    ```
    <script>

        // Array of dictionary object
        employee = [{
                id: 344,
                age: 45,
                sal: 40000,
                exp: 12,
                com: 3000
            },
            {
                id: 672,
                age: 32,
                sal: 30000,
                exp: 5,
                com: 8000
            }
        ]

    // Function to calculate total salary of a
    // Employee using employee id
    function totalIncome(id) {
        let result;

        /* Find() method takes a conditional function 
           as a parameter, array.find() method in JavaScript 
           returns the value of the first element, In the array 
           that satisfies the provided testing function */
        let empWithId = employee.find((emp) => emp.id === id);
        result = empWithId.sal + empWithId.com;
        return result;
    }

    // Printing and calling the function totalIncome()
    document.write("Total income of the Employee having" + 
                      " id:672 = " + totalIncome(672)); 

    </script>                                    
    ```

*   **输出:**

    ```
    Total income of the Employee having id:672 = 38000
    ```