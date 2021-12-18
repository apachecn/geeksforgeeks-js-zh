# JavaScript 逐位运算符

> 原文:[https://www.geeksforgeeks.org/javascript-bitwise-operators/](https://www.geeksforgeeks.org/javascript-bitwise-operators/)

下面是 JavaScript 按位运算符的例子。
**例:**

```
<script> 
var a = 4; 
var b = 1; 

document.write("A & B = " + (a & b) + '<br>'); 

document.write("A | B = " + (a | b) + '<br>'); 

document.write("~A = " + (~a) + '<br>'); 
</script>
```

**输出:**

```
A & B = 0
A | B = 5
~A = -5
```

像 C、C++、Java、Python 和各种其他语言一样，JavaScript 也支持逐位操作。在 JavaScript 中，数字存储为 64 位浮点数，但逐位操作是对 32 位二进制数执行的，即执行位操作。JavaScript 将数字转换为 32 位二进制数(带符号)，并执行该操作，然后将结果转换回 64 位数。

**下面是几个在 JavaScript 中使用的逐位逻辑运算符。**

*   **逐位 AND ( & ) :** 它是一个二进制运算符，即接受两个操作数。如果两位都被置位(即 1)，则逐位“与”(&)返回 1，在任何其他情况下返回 0。
    T20】零T23T26】一 T28】零 T30T32】一T36】零 T38T40】一 T42】一【T44

    | A | B | 产出(A&B) |
    | --- | --- | --- |
    | 零 | 零 |
    | 零 |
    | 零 |

    *   **逐位 OR ( | ) :** 它是一个二进制运算符，即接受两个操作数。如果设置了任何操作数(即 1)，则按位或(|)返回 1，在任何其他情况下返回 0。
    T24】零 T28】一 T30T32】一 T34】零 T36】一 T38T40】一 T42】一一

    | A | B | 输出(A &#124; B) |
    | --- | --- | --- |
    | 零 | 零 | 零 |
    | 一 |

    *   **逐位异或(^ ) :** 它是一个二进制运算符，即接受两个操作数。如果两个操作数不同，则逐位异或(^)返回 1，在任何其他情况下返回 0。
    t23t26】一 t28】一 t30t32】一 t34】零 t36】一 t38t40】一 t42】一【T43

    | A | B | 产出(甲^乙) |
    | --- | --- | --- |
    | 零 | 零 | 零 |
    | 零 |

    *   **Bit-Wise NOT ( ~ ) :** Its is a unary operator i.e. accepts single operands. Bit-wise NOT ( ~ ) flips the bits i.e 0 becomes 1 and 1 becomes 0.

    | A | 输出(~A) |
    | --- | --- |
    | Zero | one |
    | one | Zero |

    **下面是 JavaScript 中使用的几个逐位移位运算符。**

    1.  **左移(< < ):** 它是一个二进制运算符，即它接受两个操作数。第一个运算符指定数字，第二个运算符指定要移位的位数。每一位向左移动，0 位从右边添加。左边多余的位被丢弃。

        | A | 6(00000000000000000000000000110) |
        | --- | --- |
        | B | 1(00000000000000000001) |
        | --- | --- |
        | OUTPUT(A<<B)】 |
        | --- |

    2.  **符号传播右移(> > ) :** 它是一个二进制运算符，即它接受两个操作数。第一个操作数指定数字，第二个操作数指定要移位的位数。每一位都向右移动，溢出的位被丢弃。这是符号传播，因为从左边相加的位取决于数字的符号(即，0 表示正，1 表示负)

        | A | 6(0000000000000000000000000000000000000010) |
        | --- | --- |
        | B | 1(0000000000000000000000000000) |
        | --- | --- |

    3.  **Zero fill Right Shift ( >>> ) :** Its a binary operator i.e. it accepts two operand. The first operand specifies the number and the second operand specifies the number of bits to shift. Each bits is shifted towards right, the overflowing bits are discarded. 0 bit is added from the left so its zero fill right shift.

        | A | 6(000000000000000000000000000000110) |
        | --- | --- |
        | B | 1(00000000000000000000000001) |
        | --- | --- |
        | OUTPUT(A>>>B) | 3(000000000000000000001) |
        | --- | --- |

        **下面是上述操作符的实现。**

        ```
        <script>
        var a = 6;
        var b = 1;

        // AND Operation
        document.write("A & B = " + (a & b) + '<br>');

        // OR operation
        document.write("A | B = " + (a | b) + '<br>');

        // NOT operation
        document.write("~A = " + (~a) + '<br>');

        // Sign Propagating Right Shift
        document.write("A >> B = " + (a >> b) + '<br>');

        // Zero Fill Right Shift
        document.write("A >>> B = " + (a >>> b) + '<br>');

        // Left Shift
        document.write("A << B = " + (a << b) + '<br>'); 
        </script>                            
        ```

        **输出:**

        ```
        A & B = 0
        A | B = 7
        ~A = -7
        A >> B = 3
        A >>> B = 3
        A << B = 12
        ```

        **支持的浏览器:**

        *   谷歌 Chrome
        *   微软公司出品的 web 浏览器
        *   火狐浏览器
        *   苹果 Safari
        *   歌剧