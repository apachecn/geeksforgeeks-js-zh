# JavaScript 中的静态方法

> 原文:[https://www.geeksforgeeks.org/static-methods-in-javascript/](https://www.geeksforgeeks.org/static-methods-in-javascript/)

JavaScript 允许属于该类的静态方法，而不是该类的实例。因此，不需要实例来调用这样的静态方法。静态方法直接在类上调用。它可以是任何名字。一个类可以包含多个静态方法。如果我们定义了多个同名的静态方法，最后一个方法由 JavaScript 调用。**“this”**关键字用于在 JavaScript 中调用任何其他静态方法内的静态方法。

下面是演示如何使用和调用静态方法的 JavaScript 的不同示例。

**示例 1:** 下面是调用一个静态方法的代码。代码的*脚本*部分保存了 JavaScript 代码。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<body>

    <script>
        class GeeksforGeeks { 

            // static keyword is used 
            // before the function name
            static example1() { 

                // return the string -->
                // static method 1
                return "static method 1"
            }
        }

        // Calls the static function 
        // using className.functionName
        document.writeln(
            GeeksforGeeks.example1());
    </script>
</body>

</html>
```

**Output:**

```
static method 1

```

**示例 2:** 下面的代码演示了如何调用多个静态方法。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<body>
    <script>
        class GeeksforGeeks {

            // static keyword is used 
            // before the function name
            static example1() {

                // return the string -->
                // static method 1
                return "static method 1"
            }

            // Another static method 
            // with different name 
            static example2() {

                // return the string -->
                // static method 2
                return "static method 2"
            }

        }

        // Calls the static function using
        // className.functionName
        document.writeln(GeeksforGeeks.example1() + "<br>");
        document.writeln(GeeksforGeeks.example2());  
    </script>
</body>

</html>
```

**Output:**

```
static method 1
static method 2

```

**示例 3:** 以下示例调用了多个同名的静态方法。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<body>
    <script>
        class GeeksforGeeks {

            // static keyword is used 
            // before the function name
            static example1() {

                // returns static method 1
                return "static method 1"
            }

            // Different static method
            // with same name 
            static example1() { 

                // returns static method 2
                return "static method 2"
            }

        }

        // Calls the static function using 
        // className.functionName
        document.writeln(GeeksforGeeks.example1());
        // Invokes last static method in case 
        // if static function have same names
    </script>
</body>

</html>
```

**Output:**

```
static method 2
```

**示例 4:** 以下示例演示如何在非静态方法中调用静态方法。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<body>

    <script>
        class GeeksforGeeks { 

            // Static keyword is used 
            // before the function name
            static example1() { 

                // return the string --> 
                // static method 1
                return "static method 1"
            }

            // Non static method with 
            // different name 
            example2() { 

                // return the string -->
                // static method 1
                // Calls the static function 
                // using className.functionName
                document.writeln(GeeksforGeeks.example1());
            }
        }
        var gfg = new GeeksforGeeks();
        gfg.example2();  
    </script>
</body>

</html>
```

**Output:**

```
static method 1

```