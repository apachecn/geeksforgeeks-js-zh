# JavaScript 中有哪些工厂函数？

> 原文:[https://www . geesforgeks . org/什么是 javascript 中的工厂函数/](https://www.geeksforgeeks.org/what-are-factory-functions-in-javascript/)

工厂函数类似于构造函数/类函数，但是工厂函数只是创建一个对象并返回它，而不是使用 [*新的*](https://www.geeksforgeeks.org/javascript-new-keyword/) 来创建一个对象。

工厂函数是 JavaScript 中非常有用的工具。JavaScript 中的 Factory Functions 类似于构造函数/类函数，但它们不需要在内部值中使用“ [*”这个*](https://www.geeksforgeeks.org/this-in-javascript/) ”关键字，也不需要在实例化新对象时使用“ *new* ”关键字。工厂函数可以包含内部值、方法等。就像普通的正则函数一样。工厂函数不同于常规函数，因为它们总是返回一个对象，该对象将包含任何值、方法等。

**为什么有用？**

如果我们有复杂的逻辑，并且我们必须一次又一次地创建多个具有相同逻辑的对象，我们可以在一个函数中编写一次逻辑，并将该函数用作创建我们的对象的工厂。这和现实世界的工厂生产产品完全一样。

**示例 1:** 我们有一个工厂功能，它将生产具有单一逻辑的新机器人。利用这一点，我们可以生产出我们想要的任意多的物体/机器人。

## java 描述语言

```
<script>

    // Function creating new objects 
    // without use of 'new' keyword
    function createRobot(name) {
        return {
            name: name,
            talk: function () {
                console.log('My name is ' 
                + name + ', the robot.');
            }
        };
    }

    //Create a robot with name Chitti
    const robo1 = createRobot('Chitti');

    robo1.talk();

    // Create a robot with name Chitti 2.O Upgraded
    const robo2 = createRobot('Chitti 2.O Upgraded');

    robo2.talk();
</script>
```

**输出:**

```
My name is Chitti, the robot.
My name is Chitti 2.0 Upgraded, the robot.
```

**例 2:**

## java 描述语言

```
<script>

    // Factory Function creating person
    var Person = function (name, age) {

        // creating person object
        var person = {};

        // parameters as keys to this object  
        person.name = name;
        person.age = age;

        // function to greet
        person.greeting = function () {
            return (
                'Hello I am ' + person.name 
                    + '. I am ' + person.age 
                    + ' years old. '
            );
        };
        return person;
    };

    var person1 = Person('Abhishek', 20);
    console.log(person1.greeting());

    var person2 = Person('Raj', 25);
    console.log(person2.greeting());
</script>
```

**输出:**

```
Hello I am Abhishek. I am 20 years old. 
Hello I am Raj. I am 25 years old. 
```