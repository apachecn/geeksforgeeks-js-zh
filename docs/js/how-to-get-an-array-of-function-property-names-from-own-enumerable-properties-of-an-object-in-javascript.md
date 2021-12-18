# 如何在 JavaScript 中从对象自身的可枚举属性中获取函数属性名的数组？

> 原文:[https://www . geesforgeks . org/如何从 javascript 中的对象的自身可枚举属性中获取函数属性名称数组/](https://www.geeksforgeeks.org/how-to-get-an-array-of-function-property-names-from-own-enumerable-properties-of-an-object-in-javascript/)

**可枚举属性:**可以使用进行迭代的对象的所有属性..in loop 或 [Object.keys()方法](https://www.geeksforgeeks.org/object-keys-javascript/)被称为可枚举属性。

在本文中，我们将看到如何获取一个对象的函数数组，这些函数是**可枚举的**。这可以通过以下两个步骤来实现。

*   Using [Object.keys()](https://www.geeksforgeeks.org/object-keys-javascript/) method, we can get an array of all enumerable properties (containing functions and data members) of an Object.

    **语法:**

    ```
    Object.keys(object_name)
    ```

*   Then we can filter the above obtained array using [Array filter() method](https://www.geeksforgeeks.org/javascript-array-filter-method/) so that it contains only enumerable function names (eliminating all data members).

    **语法:**

    ```
    new_arr = arr_name.filter( (element)=> {.....} )
    ```

在下面创建不可枚举属性的实现中，我们使用了[**object . defineperoperty()方法。**T3】](https://www.geeksforgeeks.org/javascript-object-defineproperty-method/)

**例:**

## java 描述语言

```
<script>

    // Person object has name, age, salary
    // and print properties 
    // Except salary, all properties are enumerable
    let Person = {
        name: "Mahesh",
        age: 25,
        print: function () {
            console.log(`${this.name} ${(this, age)}`);
        },
    };

    // salary- non enumerable property
    Object.defineProperty(Person, "salary", {
        value: "Rs. 50,000",
        enumerable: false,
    });

    // greeting- non enumerable function
    Object.defineProperty(Person, "greeting", {
        value: function () {
            console.log("Welcome to GFG");
        },
        enumerable: false,
    });

    // arr contains all the enumerable
    // properties of Person
    let arr = Object.keys(Person);

    // functionsArr contains enumerable
    // function properties of Person.
    // typeof returns an string representing
    // data type.
    // Using filter() method to filter the array
    let functionsArr = arr.filter((key) => {
        return typeof Person[key] === "function";
    });

    console.log(arr);
    console.log(functionsArr);
</script>
```

**Output:**

```
["name", "age", "print"]
["print"]
```

**说明:**

在上面的代码中，我们有一个名为 *Person* 的对象，它有 3 个数据成员(*姓名、年龄*和*工资*)和 2 个函数(*打印】*和“*问候”*)，其中工资数据成员和问候函数是不可枚举的属性。

<figure class="table">T21T24】名称 T28】可枚举性 T30T32】年龄 T34】变量 T36】可枚举性 T38T40】工资 T42】变量

| attribute | type | Enumerability |
| --- | --- | --- |
| variable |

</figure>

这里的*打印*是唯一可枚举的功能。使用***object . keys(Person)***我们得到一个包含所有可枚举属性的数组，即[“姓名”、“年龄”、“打印”]。

然后我们用 **Array.filter()** 属性过滤掉所有变量，使数组只有函数属性名，即[“print”]。