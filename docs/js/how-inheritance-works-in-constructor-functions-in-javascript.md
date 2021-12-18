# JavaScript 中构造函数的继承是如何工作的？

> 原文:[https://www . geesforgeks . org/how-inheritation-works-in-constructor-in-functions-JavaScript/](https://www.geeksforgeeks.org/how-inheritance-works-in-constructor-functions-in-javascript/)

这里，我们将讨论在 JavaScript 中继承构造函数。构造函数定义了对象将包含的属性的原型。使用构造函数，我们可以在传递所需的参数后创建一个新的对象。

继承以前定义的构造函数意味着使用以前定义的函数的参数，同时向新定义的构造函数添加一些新参数。为此，我们需要使用[调用()](https://www.geeksforgeeks.org/javascript-function-prototype-call-method/)函数，该函数允许我们调用在当前上下文中其他地方定义的函数。

**语法:**

```
myFunction.call( this, property1, property2, ... , propertyN )
```

**参数值:**

*   **my function:** This is a constructor from which we want to inherit the parameters in a new constructor.
*   **This** : The parameter value of the keyword [and](https://www.geeksforgeeks.org/this-in-javascript/) will be used when calling myFunction.
*   **Property1, property2, …, Propertyn:** Parameters to be inherited in the new constructor.

**返回类型:**构造函数或继承了其属性的函数没有任何返回类型。它指定了对象将包含的属性的**原型**，这些属性是从该构造函数创建的。

**示例:**这里，我们创建一个‘雇员’构造函数。创建了一个新的“开发人员”构造函数，它将继承“员工”的基本属性，并包含一些新属性。

## HTML

```
<!DOCTYPE html>
<html lang="en">

<head>
    <title> 
        JavaScript inheritence of constructor functions 
    </title>
</head>

<body>
    <script>
        function Employee(name, age, gender, id) {
            this.name = name;
            this.age = age;
            this.gender = gender;
            this.id = id;
        };

        function Developer(name, age, gender, id, 
        specialization) {

            // Calling Employee constructor function
            Employee.call(this, name, age, gender, id);

            // Adding a new parameter
            this.specialization = specialization;
        }
        console.log(Employee.prototype);
        console.log(Developer.prototype);
    </script>
</body>

</html>
```

**输出:**

```
Object
constructor: ƒ Employee(name, age, gender, id)
[[Prototype]]: Object

Object
constructor: ƒ Developer(name, age, gender, id, specialization)
[[Prototype]]: Object
```

我们可以注意到“ **Developer** ”构造函数继承了“ **Employee** ”构造函数的属性以及一个新参数“**专门化**”。这里，我们使用 call()函数调用了 Employee 函数，将所需的参数传递给 Employee 构造函数。

我们还可以在传递对象的必需属性值之后，使用这些构造函数创建对象。

**语法:**

```
let Obj1 = new Object( parameters )
```

**示例:**本示例描述了使用 [new](https://www.geeksforgeeks.org/javascript-new-keyword/) 关键字创建的对象，以创建具有构造函数的对象实例。

## HTML

```
<!DOCTYPE html>
<html lang="en">

<head>
    <title> 
        JavaScript inheritence of constructor functions
     </title>
</head>

<body>
    <script>
        function Employee(name, age, gender, id) {
            this.name = name;
            this.age = age;
            this.gender = gender;
            this.id = id;
        };

        function Developer(name, age, gender, id, specialization) {

            // Calling Employee constructor function
            Employee.call(this, name, age, gender, id);

            // Adding a new parameter
            this.specialization = specialization;
        }

        // Creating objects
        let Employee1 = new Employee("Suraj", 28, "Male", 564);
        let Developer1 = new Developer("Karishma", 31, "Female", 345,
            "Frontend Developer");
        console.log(Employee1);
        console.log(Developer1);
    </script>
</body>

</html>
```

**输出:**

```
Employee {name: 'Suraj', age: 28, gender: 'Male', id: 564}
age: 28
gender: "Male"
id: 564
name: "Suraj"
[[Prototype]]: Object

Developer {name: 'Karishma', age: 31, gender: 'Female', id: 345, 
    specialization: 'Frontend Developer'}
age: 31
gender: "Female"
id: 345
name: "Karishma"
specialization: "Frontend Developer"
[[Prototype]]: Object
```

我们可以观察到 Employee 的构造函数是继承的，以创建一个新的构造函数 Developer，它可以用来创建具有新属性的对象以及父构造函数的继承属性。