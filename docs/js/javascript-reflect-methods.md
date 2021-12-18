# JavaScript 反映方法

> 原文:[https://www.geeksforgeeks.org/javascript-reflect-methods/](https://www.geeksforgeeks.org/javascript-reflect-methods/)

**Reflect** 是一个内置的 JavaScript 对象，可以访问其他方法进行可拦截的操作。JavaScript Reflect 方法与代理处理程序的方法相同，是静态的，就像[数学](https://www.geeksforgeeks.org/javascript-math-object/)对象一样。因为它不是 JavaScript 函数对象，所以不可构造。它不能与 JavaScript new 运算符一起使用，也不能作为函数调用。

**静态方法:** JavaScript Reflect 对象提供了以下静态方法。

1.  [反映.应用(目标，此参数，参数列表)](https://www.geeksforgeeks.org/javascript-reflect-apply-method/#:~:text=The%20Reflect.,prototype.)
2.  [Reflect.construct(target，argumentsList[，newTarget])](https://www.geeksforgeeks.org/javascript-reflect-construct-method/#:~:text=The%20Reflect.,to%20specify%20a%20different%20prototype.)
3.  [反射.定义属性(目标，属性键，属性)](https://www.geeksforgeeks.org/javascript-reflect-defineproperty-method/#:~:text=The%20Reflect.,the%20property%20was%20successfully%20defined.)
4.  [Reflect.deleteProperty(目标，propertyKey)](https://www.geeksforgeeks.org/javascript-reflect-deleteproperty-method/)
5.  [Reflect.get(target，propertyKey[，receiver])](https://www.geeksforgeeks.org/javascript-reflect-get-method/#:~:text=The%20Reflect.,the%20value%20of%20the%20property.)
6.  [reflect . GetownPropertyDescriptor(目标，属性键)](https://www.geeksforgeeks.org/javascript-reflect-getownpropertydescriptor-method/)
7.  [Reflect.getPrototypeOf(目标)](https://www.geeksforgeeks.org/javascript-reflect-getprototypeof-method/)
8.  [反射具有(目标，属性键)](https://www.geeksforgeeks.org/javascript-reflect-has-method/)
9.  [reflect . iseextensible(目标)](https://www.geeksforgeeks.org/javascript-reflect-isextensible-method/)
10.  [Reflect.ownKeys(目标)](https://www.geeksforgeeks.org/javascript-reflect-ownkeys-method/#:~:text=The%20Reflect.,it%20ignores%20the%20inherited%20properties.)
11.  [反映.预防措施(目标)](https://www.geeksforgeeks.org/javascript-reflect-preventextensions-method/)
12.  [反射集(目标，属性键，值[，接收器])](https://www.geeksforgeeks.org/javascript-reflect-set-method/#:~:text=The%20Reflect.,value%20of%20an%20object%20property.&text=Parameters%3A%20This%20method%20accept%20four,used%20to%20set%20the%20property.)
13.  [反射.设定(目标，原型)的旋转类型](https://www.geeksforgeeks.org/javascript-reflect-setprototypeof-method/#:~:text=The%20Reflect.,the%20operation%20that%20are%20successful.)

下面是 JavaScript 反射对象方法的例子。

**示例 1:** 以下示例演示了 *Reflect.has(target，propertyKey)* 方法，如果目标参数*具有*属性，则该方法返回一个 [布尔](https://www.geeksforgeeks.org/javascript-boolean/) 。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" 
        content="width=device-width, initial-scale=1.0" /> 
</head>
<body>

  <script type='text/javascript'>

    const car = {
      name: 'Maruti',
      color: 'white',
      model: '2019'
    }

    // If the target has the property, it returns a Boolean.    
    // It acts like the in operator in a function.
    console.log("car object has 'color' property :", 
                             Reflect.has(car, 'color'));
    console.log("car object has 'haircut' property :",
                             Reflect.has(car, 'haircut'));

  </script>
</body>
</html>
```

**输出:**

```
car object has 'color' property : true
car object has 'haircut' property : false
```

**示例 2:** 以下示例演示了 *Reflect.ownKeys(目标)方法*，该方法返回是目标参数自身属性键的数组。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>

  <meta charset="UTF-8" />
  <meta name="viewport" 
   content="width=device-width, initial-scale=1.0" /> 
</head>
<body>
   <script type='text/javascript'>

    const car = {
      name: 'Maruti',
      color: 'white',
      model: '2019'
    }

    // It returns an array of the target's
    // own property keys.
    console.log("All the keys of the object 'car':", 
                                   Reflect.ownKeys(car));
  </script>
</body>
</html>
```

**输出:**

```
All the keys of the object 'car': (3)
["name", "color", "model"]
```

**示例 3 :** 以下示例演示了 *Reflect.set(目标，属性键，值[，接收器])* 方法，该方法将值分配给返回 *true* 布尔值的属性。如果*反射设置*成功，则返回*真*否则返回*假*。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" 
      content="width=device-width, initial-scale=1.0" /> 
</head>
<body>

  <script type='text/javascript'>

    const car = {
      name: 'Maruti',
      color: 'white',
      model: '2019'
    }

    // It assigns values to properties. 
    // It returns true if the set or update is successful.
    console.log("Insert key : 'airbags' to the object 'car':", 
                             Reflect.ownKeys(car, 'airbags', 3));
    console.log(car);
  </script>
</body>

</html>
```

**输出:**

```
Insert key : 'airbags' to the object 'car': (3)
["name", "color", "model"]
{name: "Maruti", color: "white", model: "2019"}
```

**示例 4:** 以下示例演示了***【reflect . apply(target，thisArgument，argumentsList)* 其中 c 调用 target 函数，参数在 *argumentsList* 中。**

## **超文本标记语言**

```
<!DOCTYPE html>
<html lang="en">

<head>

  <meta charset="UTF-8" />
  <meta name="viewport" 
      content="width=device-width, initial-scale=1.0" /> 

</head>

<body>
   <script type='text/javascript'>

    // It calls a target function with the 
    // argumentsList as parameter.
    console.log(Reflect.apply(String.fromCharCode, 
                   undefined, [103, 101, 101, 107, 115]));

    console.log(Reflect.apply(Math.floor, undefined, [3.14]));

    console.log(Reflect.apply(RegExp.prototype.exec, /ab/, 
                                    ['confabulation']).index);

    console.log(Reflect.apply(''.charAt, 'geeksforgeeks', [6]));

  </script>
</body>

</html>
```

****输出:****

```
geeks
3
4
o
```