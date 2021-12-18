# 如何在 JavaScript 中扩展对象？

> 原文:[https://www . geesforgeks . org/如何在 javascript 中扩展对象/](https://www.geeksforgeeks.org/how-to-extend-an-object-in-javascript/)

**扩展**关键字可以用来扩展 JavaScript 中的对象和类。它通常用于创建另一个类的子类。

**语法:**

```
class childclass extends parentclass {...}
class parentclass extends in-built object {...}

```

下面的例子描述了一个子类如何使用关键字**扩展**并通过创建子类的对象来使用父类的属性。在示例 1 中，我们看到类 Profile 有两个属性名称和年龄。现在，我们将看到学生类使用关键字**通过添加属性语言扩展**来获取类配置文件的两个属性，然后显示所有属性。

**示例 1:** 在本例中，我们使用了 **extends** 关键字。

*   **程序:**

    ```
    <script>

        // Declaring class
        class Profile { 

            // Constructor of profile class
            constructor(name, age) { 
                this.name = name;
                this.age = age;
            }

            getName() {

                // Method to return name
                return this.name; 
            }

            getAge() {

                // Method to return age
                return this.age; 
            }

            getClass() {
                return this;
            }
        }

    // Class Student extends class Profile 
    class Student extends Profile { 

        // Each data of class Profile can be
        // accessed from student class.
        constructor(name, age, languages) {

            // Acquiring of attributes of parent class
            super(name, age); 
            this.lang = [...languages];
        }

        // Method to display all attributes
        getDetails() {
            console.log("Name : " + this.name);
            console.log("Age : " + this.age);
            console.log("Languages : " + this.lang);
        }
    }

    // Creating object of child class with passing of values
    var student1 = new Student("Ankit Dholakia", 24,
                ['Java', 'Python', 'PHP', 'JavaScript']);
    student1.getDetails(); 
    </script>
    ```

*   **输出:**

    ```
    Name : Ankit Dholakia
    Age : 24
    Languages : Java,Python,PHP,JavaScript

    ```

**示例 2:** 在本例中，我们将看到如何使用扩展语法将两个对象扩展成第三个对象，并显示两个对象的包含属性。

*   **程序:**

    ```
    <script>
    // Creating first object
    var obj1 = { 
         name: 'Ankit',
         age: 20
    };

    // Creating second object
    var obj2 = { 
        marks: 50
    };

    // Using spread syntax to extend
    // both objects into one
    var object = {
        ...obj1,
        ...obj2
    };
    console.log(object); 
    </script>
    ```

*   **输出:**

    ```
    { name: 'Ankit', age: 20, marks: 50 }

    ```