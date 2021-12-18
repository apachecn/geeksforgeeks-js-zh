# ES6 类和 ES5 函数构造函数的区别

> 原文:[https://www . geesforgeks . org/differences-es6-class-and-es5-function-constructors/](https://www.geeksforgeeks.org/differences-between-es6-class-and-es5-function-constructors/)

在本文中，我们将讨论 ES6 类和 ES5 函数构造函数之间的区别。两者都服务于创建新对象的目的，尽管如此，它们之间还是有一些差异。

**ES6 类构造函数:** ES6 类构造函数的工作方式与其他面向对象语言中的类构造函数完全相同。它们用于创建新对象。

## java 描述语言

```
<script>
    class User {
        constructor(name, age, gender) {
            this.name = name;
            this.age = age;
            this.gender = gender;
        }
        print() {
            console.log(`${this.name} has an age of 
            ${this.age} and gender of ${this.gender}`);
        }
    }

    const Roy = new User('Roy', '19', 'Male');
    Roy.print();
</script>
```

**输出:**

```
"Roy has an age of 19 and gender of Male"
```

**ES5 函数构造函数:** ES5 函数构造函数也用于创建对象。通过使用函数构造函数，上面的例子可以修改如下。

## java 描述语言

```
<script>
    function User(name, age, gender) {
        this.age = age;
        this.name = name;
        this.gender = gender;
        this.print = function () {
            console.log(
                `${this.name} has an age of ${this.age} 
                and gender of ${this.gender}`
            );
        };
    }

    const Roy = new User('Roy', '19', 'Male');
    Roy.print();
</script>
```

**输出:**

```
"Roy has an age of 19 and gender of Male"
```

**ES6 类与 ES5 函数构造函数的区别:**

<figure class="table">

| **ES6 constructor** | **ES5 function constructor** |
| --- | --- |
| As mentioned above, ES6 class constructors create objects by adding functions to their prototypes (blueprints). | The ES5 function constructor also creates objects with inherited attributes. |
| It ensures that the keyword *used by developers refers to the object being created by developers.* | Any function can be used as a function constructor, which focuses on the creation of reusable object creation code. |
| Its syntax is similar to object creation in other object-oriented programming languages. | Its syntax is unique and can't be found in other object-oriented programming languages. |
| This can be said to be the grammatical basis of constructors, and new operators are used to instantiate objects. | This also uses a new operator to create the object, but focuses on how the object is instantiated. |

</figure>