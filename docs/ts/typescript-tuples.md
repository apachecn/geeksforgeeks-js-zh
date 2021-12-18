# 类型脚本元组

> 原文:[https://www.geeksforgeeks.org/typescript-tuples/](https://www.geeksforgeeks.org/typescript-tuples/)

众所周知，数组由同构类型的值组成，但有时我们需要在单个变量中存储不同类型值的集合。那我们就用**元组**去。它们就像 C 编程中的结构，也可以在函数调用中作为参数传递。

*   为了表示多维坐标系，在抽象数学中使用的术语是元组。*   In JavaScript we doesn’t have tuples as data types, but in typescript Tuples facility is available.

    **语法**

    ```
    let tuple_name = [val1, val2, val3, ...val n];  

    ```

    **示例:**

    ```
    let arrTuple = [501, "welcome", 505, "Mohan"];  
    console.log(arrTuple);

    ```

    **输出:**

    > [501，“欢迎”，105，“莫汉”]

    通过在 Typescript 中将元组初始声明为空元组来分别声明和初始化元组。
    **例:**

    ```
    let arrTuple = [];   
    arrTuple[0] = 501  
    arrTuple[1] = 506 

    ```

    **访问元组元素**
    借助索引基础，我们可以读取或访问元组的字段，这与数组相同。索引也是从零开始的。
    **例:**

    ```
    var employee: [number, string] = [1, "Steve"];
    employee[0]; // returns 1
    employee[1]; / return Steve

    ```

    **输出:**

    > 1
    > 史蒂夫

    我们可以在元组中同时声明异构数据类型，如:number 和 string。
    **例**

    ```
    let empTuple = ["Vivek Singh", 22, "Honesty"];  
    console.log("Name of the Employee is : "+empTuple [0]);  
    console.log("Age of the Employee is : "+empTuple [1]);  
    console.log(empTuple [0]+" is workinging in "+empTuple [2]);  

    ```

    输出:

    > 员工姓名:维维克·辛格
    > 员工年龄:22
    > 维维克·辛格在微软工作

    **元组上的操作**
    元组有两个操作:

    *   推送()*   Pop()

    **Push()**
    通过 Push 操作向元组中添加元素。
    **示例**

    ```
    var employee: [number, string] = [1, "Steve"];
    employee.push(2, "Bill"); 
    console.log(employee); 

    ```

    **输出:**

    > [1，“史蒂夫”，2，“比尔”]

    元组中允许这种类型的声明，因为我们正在向元组中添加数字和字符串值，它们对**员工**元组有效。
    **例**

    ```
    let empTuple = ["Vivek Singh", 22, "Honesty"];  
    console.log("Items: "+empTuple);   // here we print tuple elements
    empTuple.push(10001);   // append value to the tuple   
    console.log("Length of Tuple Items after push: "+empTuple.length);  // After pushing elements in tuples calculate length of tuples.
    console.log("Items: "+empTuple);  

    ```

    **输出:**

    > 项目:维维克·辛格，22，诚实
    > 推送后元组项目长度:4
    > 项目:维维克·辛格，22，诚实，10001

    使用推送操作向元组中添加元素。
    **例**

    ```
    let empTuple = ["Mohit Singh", 25, "geeksforgeeks", 10001];  
    console.log("Items: "+empTuple);   // here we print tuple elements
    empTuple.pop();   // removed value to the tuple   
    console.log("Length of Tuple Items after pop: "+empTuple.length);  After pushing elements in tuples calculate length of tuples.
    console.log("Items: "+empTuple);  

    ```

    **输出:**

    > 物品:莫希特·辛格，25 岁，极客们，10001
    > 爆料后元组物品长度:3
    > 物品:莫希特·辛格，25 岁，极客们，极客们

    **更新或修改元组元素**
    我们需要使用字段的索引和赋值运算符来修改元组的字段。可以在下面的示例中显示。
    **示例**

    ```
    let empTuple = ["Ganesh Singh", 25, "TCS"];  
    empTuple[1] = 60;  
    console.log("Name of the Employee is: "+empTuple [0]);  
    console.log("Age of the Employee is: "+empTuple [1]);  
    console.log(empTuple [0]+" is workinging in "+empTuple [2]); 

    ```

    **输出:**

    > 员工姓名:甘尼什·辛格
    > 员工年龄:60
    > 甘尼什·辛格在 TCS 工作

    **清除元组的字段**
    字段可以被清除，但是我们不能删除元组变量。要清除元组的字段，请为其分配一个空的元组字段集，如下所示:

    ```
    let empTuple = ["Rohit Sharma", 25, "JavaTpoint"];  
    empTuple = [];  
    console.log(empTuple); 

    ```

    **输出:**

    > []

    在类型脚本中，通过析构来分解实体的结构。
    **例**

    ```
    let empTuple = ["Rohit Sharma", 25, "JavaTpoint"];  
    let [emp, student] = empTuple;  
    console.log(emp);  
    console.log(student);  

    ```

    > 罗希特·夏尔马
    > 25

    **将元组传递给函数**

    ```
    //Tuple Declaration  
    let empTuple = ["JavaTpoint", 101, "Abhishek"];     
    //Passing tuples in function    
    function display(tuple_values:any[]) {    
       for(let i = 0;i<empTuple.length;i++) {     
          console.log(empTuple[i]);    
       }      
    }    
    //Calling tuple in function    
    display(empTuple);

    ```

    > JavaTpoint
    > 101
    > Abhishek