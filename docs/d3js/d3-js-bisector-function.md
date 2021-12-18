# D3.js 平分线()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-bisector-function/](https://www.geeksforgeeks.org/d3-js-bisector-function/)

D3.js 中的**平分线()函数**用于使用指定的访问器或比较器函数返回新的平分线。这种方法可以用来平分对象数组，而不是局限于简单的基元数组。

**语法:**

```
d3.bisector(accessor)
d3.bisector(comparator)
```

**参数:**该函数只接受一个参数，上面提到了，下面描述了:

*   **存取器/比较器:**此参数是可以是存取器或比较器的功能。

**返回值:**该函数返回新的平分线。

下面给出了上述函数的几个例子。

**示例 1:** 该程序使用访问器参数说明了 d3 .等分线()的使用。

```
<!DOCTYPE html> 
<html> 

<head> 
    <title>D3.js d3.bisector() Function</title> 

    <script src='https://d3js.org/d3.v4.min.js'>
   </script> 
</head> 

<body> 
    <script> 
        var data = [
          {date: new Date(2011, 1, 1), value: 0.5},
          {date: new Date(2012, 2, 1), value: 0.6},
          {date: new Date(2013, 3, 1), value: 0.7},
          {date: new Date(2014, 4, 1), value: 0.8}
        ]; 

        var bisectDate = 
d3.bisector(function(d) { return d.date; }).left; 
        var dat = new Date(2014, 4, 1);
        document.write(bisectDate(data, dat)); 
    </script> 
</body> 

</html>
```

**输出:**

```
3
```

**示例 2:** 该程序使用比较器函数参数说明了 d3 .等分线()的使用。

```
<!DOCTYPE html> 
<html> 

<head> 
    <title>D3.js d3.bisector() Function</title> 

    <script src='https://d3js.org/d3.v4.min.js'>
    </script> 
</head> 

<body> 
    <script> 
        var data = [
          {date: new Date(2011, 1, 1), value: 0.5},
          {date: new Date(2012, 2, 1), value: 0.6},
          {date: new Date(2013, 3, 1), value: 0.7},
          {date: new Date(2014, 4, 1), value: 0.8}
        ]; 

        var bisectDate = 
d3.bisector(function(d, x) { return d.date - x; }).right;
        var dat = new Date(2014, 4, 1);
        document.write(bisectDate(data, dat)); 
    </script> 
</body> 

</html>
```

**输出:**

```
4
```