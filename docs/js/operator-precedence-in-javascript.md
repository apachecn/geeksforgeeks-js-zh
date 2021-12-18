# JavaScript 中的运算符优先级

> 原文:[https://www . geeksforgeeks . org/operator-preference-in-JavaScript/](https://www.geeksforgeeks.org/operator-precedence-in-javascript/)

运算符优先级是指在解析包含多个运算符的语句时赋予运算符的优先级。确保正确的结果以及帮助编译器理解操作的顺序是很重要的。优先级较高的运营商优先解决。但是，随着一个人进入列表，优先级会降低，因此他们的分辨率也会降低。

**优先和结合性:**结合性一般来说，不管给定操作的操作数顺序如何，结果都保持不变。优先级用于告诉编译器应该首先执行什么操作。例如，考虑三个数字 2、3 和 4。现在考虑两个操作:

```
( 2 + 3 ) + 4 = 2 + ( 3 + 4 )
( 2 >= 3 ) or ( 1 != 4 )
```

第一个操作是**关联性**，顺序无关紧要。第二种情况是优先，为了达到预期的结果，必须有一个正确的操作执行顺序。

结合性不是一个单一的概念，而处理优先操作必须处理从左到右或从右到左的结合性。这完全取决于操作，并告诉解析器操作应该从哪个方向开始。

**示例:**

```
// left-to-right associativity : division 
3/4

```

```
// right-to-left associativity : assignment 
a = 3 

```

**运算符优先级表:**运算符优先级表可以帮助人们了解一个运算符相对于其他运算符的优先级。当一个操作符进入表中时，这些操作符的优先级相互递减，也就是说，一个操作符的优先级低于它上面的操作符，高于它下面的操作符。同一行中的运算符具有相同的优先级。

在该表中，1 是最高优先级，19 是最低优先级。

<figure class="table">

```
 | **Precedence ** | **Operator** | **Description** | **Associativity** | **Example** |
| 1 | () | Grouping | – | (1+2) |
| 2 | . | Member | left to right | obj.function |
| [] | Member | left to right | obj[“func”] |  |
| new | Create | – | new Date() |  |
| () | Function call | left to right | func() |  |
| 3 | ++ | Postfix increment | – | i++ |
| — | Postfix decrement | – | i– |  |
| 4 | ++ | Prefix increment | right to left | ++i |
| — | Prefix decrement | –i |  |  |
| ! | Logical NOT | !TRUE |  |  |
| typeof | Type | typeof a |  |  |
| 5 | ** | Exponentiation | right to left | 4**2 |
| 6 | * | Multiplication | left to right | 2*3 |
| / | Division | 18/9 |  |  |
| % | Remainder | 4%2 |  |  |
| 7 | + | Addition | left to right | 2+4 |
| – | Subtraction | 4-2 |  |  |
| 8 | <<  | Left shift  | left to right | y<<2 |
| >>  | Right shift | y>>2 |  |  |
| >>>  | Unsigned Right shift  | y>>>2 |  |  |
| 9 | <  | Less than | left to right | 3<4 |
| <=  | Less than or equal | 3<=4 |  |  |
| >  | Greater than | 4>3 |  |  |
| >=  | Greater than or equal | 4>=3 |  |  |
| in | In | “PI” in MATH |  |  |
| instanceof | Instance of  | A instanceof B |  |  |
| 10 | == | Equality | left to right | x==y |
| != | Inequality | x!=y |  |  |
| === | Strictly equal | x===y |  |  |
| !== | Strictly unequal | x!==y |  |  |
| 11 | & | Bitwise AND | left to right | x&y |
| 12 | ^ | Bitwise XOR | left to right | x^y |
| 13 | | | Bitwise OR | left to right | x|y |
| 14 | && | Logical AND | left to right | x&&y |
| 15 | || | Logical OR | left to right | x||y |
| 16 | ? : | Conditional | right to left | (x>y)?x:y |
| 17 |   | Assignment | right to left | x=5 |
| += | x+=3 |  |  |  |
| -= | x-=3 |  |  |  |
| *= | x*=3 |  |  |  |
| /= | x/=3 |  |  |  |
| %= | x%=3 |  |  |  |
| <<=  | x<<=2 |  |  |  |
| >>=  | x>>=2 |  |  |  |
| >>>=  | x>>>=2 |  |  |  |
| &= | x&=y |  |  |  |
| ^= | x^=y |  |  |  |
| |= | x|=y |  |  |  |
| 18 | yield | Pause function  | right to left | yield x |
| 19 | , | Comma | left to right | x,y | 
```

</figure>