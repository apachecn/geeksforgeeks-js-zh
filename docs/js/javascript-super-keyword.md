# JavaScript |超级关键词

> 原文:[https://www.geeksforgeeks.org/javascript-super-keyword/](https://www.geeksforgeeks.org/javascript-super-keyword/)

JavaScript 中的 Super 关键字可以用来访问和调用对象的父对象，它可以有两种使用方式。

*   **作为函数**
*   **作为对象**

**语法:**

```
super(arguments);
super.parentMethod(arguments);
```

**参数:**这个关键字可以接受所有已经用来创建构造函数的参数。

下面的例子说明了超级关键字在 JavaScript 中的用法。

**示例:**在**时装设计师** **类**的构造函数中，super 已经被用作函数。而在**时装设计师** **类**的 **doTasks()函数**中，super 被用作对象。在时装设计师类的构造函数中，super 关键字被用作一个函数，通过将参数传递给时装设计师来调用父类的构造函数。这一步很重要，要确保**时尚设计师**是人的实例。在 **doTasks()函数**中，super 用作引用父类 Person 实例的对象。这里，super 关键字用于显式调用父类 Person 的方法。

## java 描述语言

```
<!DOCTYPE html>
<html>
    <head> </head>
    <body>
        <script>
            class Person {
                constructor(name, age) {
                    this.name = name;
                    this.age = age;
                }
                atWork() {
                    return this.name + " is at work, ";
                }
                atHome() {
                    return this.name + " is at home";
                }
                sleeping() {
                    return this.name + " is sleeping";
                }
            }
            class FashionDesigner extends Person {
                constructor(name, age) {
                    super(name, age);
                }
                profession() {
                    return this.name +
                      " is a Fashion Designer";
                }
                doTasks() {
                    return super.atWork() + this.profession();
                }
            }
            function display(content) {
                console.log(content);
            }
            const character =
            new FashionDesigner("Sayan", 30);
            display(character.profession());
            display(character.atHome());
            display(character.doTasks());
        </script>
    </body>
</html>
```

**输出:**

```
Sayan is a Fashion Designer
Sayanis at home
Sayanis at work Sayan is a Fashion Designer
```