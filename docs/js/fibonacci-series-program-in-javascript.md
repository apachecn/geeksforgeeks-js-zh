# JavaScript 中的斐波那契数列程序

> 原文:[https://www . geesforgeks . org/Fibonacci-series-program-in-JavaScript/](https://www.geeksforgeeks.org/fibonacci-series-program-in-javascript/)

假设在一堂课上，老师让 1 号卷的学生在黑板上写 0，2 号卷的学生写 1，并让其余的学生写你前面两个学生的总和。写在黑板上的数列看起来像 0，1，1，2，3，5，8，…

老师接着告诉学生，这个数列被称为**斐波那契数列**。它可以用下面的等式表示

```
 Fn = Fn-1 + Fn-2
```

其中 F0=1，F1=1。斐波那契数列是下列整数序列中的数字 0，1，1，2，3，5，8，13，21，34，55，89，144，…..在数学术语中，斐波那契数列 Fn 由递归关系定义

```
Fn = Fn-1 + Fn-2 with seed values F0 = 0 and F1 = 1
```

**示例:**

```
Input : 5 
Output : 8

Input :8
Output :34

```

因为第一个斐波那契数是 0，第二个是 1。另外，我们知道第 n 个斐波那契数是 n-1 和 n-2 项的和。
所以，要得到第 n 个斐波那契项，我们可以遵循
fib(1)= 0
fib(2)= 1
fib(3)= fib(2)+fib(1)
fib(4)= fib(3)+fib(2)
…。
fib(n)=fib(n-1)+fib(n-2)

**示例:**通过使用 for 循环

## java 描述语言

```
<script type = "text/javascript">
function fibonacci(num)
{
    var num1=0;
    var num2=1;
    var sum;
    var i=0;
    for (i = 0; i < num; i++) 
    {
        sum=num1+num2;
        num1=num2;
        num2=sum;
    }
    return num2;
}

document.write("Fibonacci(5): "+fibonacci(5)+"<br>");
document.write("Fibonacci(8): "+fibonacci(8)+"<br>");
</script>
```

**输出:**

```
Fibonacci(5): 3
Fibonacci(8): 13
```

**示例:**通过使用 while 循环

## java 描述语言

```
<script type = "text/javascript">
function fibonacci(num)
    {
        if(num==1)
            return 0;
        if(num==2)
            return 1;
        var num1=0;
        var num2=1;
        var sum;
        var i=2;
        while (i<num)  
        {
            sum=num1+num2;
            num1=num2;
            num2=sum;
            i+=1;
        }
        return num2;
    }

document.write("Fibonacci(5): "+fibonacci(5)+"<br>");
document.write("Fibonacci(8): "+fibonacci(8)+"<br>");
</script>
```

**输出:**

```
Fibonacci(5): 3
Fibonacci(8): 13
```

**通过使用递归:**我们知道，第 n 个斐波那契数是 n-1 和 n-2 项的和，n-1 项是 n-2 和 n-3 项的和。
所以，要得到第 n 个斐波那契项，我们可以遵循
fib(n)= fib(n-1)+fib(n-2)
fib(n)= fib(n-2)+fib(n-3)+fib(n-3)+fib(n-4)
…。
fib(n)= fib(1)+fib(0)+fib(1)+fib(0)+fib(1)+fib(0)…。fib(1)+fib(0)[包含 fib(1)和 fib(0)
fib(1)=0
fib(2)=1 的术语

**示例:**

## java 描述语言

```
<script type = "text/javascript">
function fibonacci(num)
    {   
        if(num==1)
            return 0;
        if (num == 2)
            return 1;
        return fibonacci(num - 1) + fibonacci(num - 2);
    }
document.write("Fibonacci(5): "+fibonacci(5)+"<br>");
document.write("Fibonacci(8): "+fibonacci(8)+"<br>");
</script>
```

**输出:**

```
Fibonacci(5): 3
Fibonacci(8): 13
```