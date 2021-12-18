# JavaScript object . prototype . _ _ lookupGetter _ _()方法

> 原文:[https://www . geesforgeks . org/JavaScript-object-prototype-_ _ lookup getter _ _-method/](https://www.geeksforgeeks.org/javascript-object-prototype-__lookupgetter__-method/)

JavaScript**object . prototype . _ _ lookupGetter _ _()**方法返回一个作为 Getter 绑定到指定属性的函数。虽然不建议使用此方法，但现在已不推荐使用。

**语法:**

```
__lookupGetter__(sprop)
```

**参数:sprop** 是一个字符串，表示将返回其 getter 的属性的名称。

**返回值:**返回绑定到指定属性的函数。

下面是一些如何使用这种方法的例子。

**例 1:**

## Javascript

```
<script>

// Created a cal object and set
// up a getter add()
var cal = {
    get add() { 
        var x=8;
        var y=10;
        return x+y;
    }
}

// This method returns a function 
console.log(typeof(cal.__lookupGetter__('add')));
</script>
```

**输出:**

```
function
```

**例二:**

## Javascript

```
<script>
    var cal = {

        get add() {
            var x = 8;
            var y = 10;
            return x + y;
        },
        get multiply() {
            var x = 8;
            var y = 10;
            return x * y;
        }
    }

    console.log(cal.__lookupGetter__('add')());
    console.log(cal.__lookupGetter__('multiply')());
</script>
```

**输出:**

```
18
80
```

**__lookupGetter()** 方法正在返回作为 Getter 绑定的函数 *add()* 和*乘()*。