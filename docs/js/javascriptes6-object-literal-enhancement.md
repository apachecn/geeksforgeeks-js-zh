# JavaScript(ES6) |对象文字增强

> 原文:[https://www . geesforgeks . org/JavaScript 6-对象-文字-增强/](https://www.geeksforgeeks.org/javascriptes6-object-literal-enhancement/)

对象文字增强用于将全局范围内的变量分组，并将其形成 javascript 对象。这是重组或重新组合的过程。

**例 1:**

```
<script>
// variable declaration
var name = "Duke";
var color = "Brown";
var age = 5;

// Using Object Literal Enhancement
// Combines all variables into a dog object
var dog = {name, color, age};
console.log(dog);
</script>
```

**输出:**名称、颜色、年龄现在是**狗**对象的关键。

```
{
    name:"Duke",
    color:"Brown",
    age:5
}

```

**示例 2:** 我们还可以创建带有对象文字增强的对象方法。

```
<script>
// variable declaration
var name = "Tike";
var color = "Black";
var age = 7;

// function declaration
var bark = function(){
    console.log("Woof Woof!!");
}

// Using Object Literal Enhancement
// combines all variables into an anotherDog object
var anotherDog = {name, color, age, bark};
anotherDog.bark();
</script>
```

**输出:**

```
Woof Woof!!
```

**例 3:** 我们也可以使用**“这个”**关键字来访问对象键。

```
<script>
    // Variable declaration
    var name = "Lilly";
    var color = "White";
    var age = 3;

    // function declaration 
    // using "this" keyword to access the object keys.
    var barkWithName = function(){
        console.log('Woof Woof!!, I am '
        +this.name+' and I am a '
        +this.age+' years old, '
        +this.color+ ' coloured dog.Woof Woof!!');
    }

    // Using Object Literal Enhancement
    // combines all variables into a yetAnotherDog object
    var yetAnotherDog = {name, color, age, barkWithName};
    yetAnotherDog.barkWithName();
</script>                    
```

**输出:**

```
Woof Woof!!, I am lilly and I am a 3 years old,
white coloured dog.Woof Woof!!
```

**例 4:** 定义对象方法时，不再需要使用**函数**关键字。对象文字增强允许我们将全局变量拉入对象，并通过使<strng>函数关键字变得不必要来减少键入。</strng>

```
<script>
// Old syntax
var driver1 = {
    name: "John",
    speed: 50,
    car:"Ferrari",
    speedUp: function(speedup){
         this.speed = this.speed + speedup;
         console.log("new speed = "+ this.speed)
    }
}

// New syntax without function keyword
const driver2 = {
    name: "Jane",
    speed: 60,
    car:"McLaren",
    speedUp(speedup){
         this.speed = this.speed + speedup;
         console.log("new speed = "+ this.speed)
    }
}
</script>
```