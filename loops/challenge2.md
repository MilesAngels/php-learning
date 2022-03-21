# Challenge 2: Fibonacci Sequence up to n Number Of Terms
## Problem Statement
- In this exercise, you have to write Fibonacci Sequence of a given number.
    - You have to print the sequence up to the given range.
    - There is a string variable ans given in which you have to store all the Fibonacci values computed up to the given range by appending them.
        - Here’s a link showing how you can add values to a string.

>`<?php`
>&#09;`$range = 6; //this will be the range of the fibonacci sequence`
>&#09;`//$ans = ""; //this will be the output`
>&#09;`$num1 = 0; // 1st value in the fibonacci sequence`
>&#09;`$num2 = 1; //2nd value in the fibonacci sequence`
>&#09;`$fibonacci = 0;`
>&#09;`echo "Fibonacci Series upto $range Terms \n";`
>&#09;`for($i = 0; $i < $range; $i++) {`
>&#09;&#09;`if($i <= 1){`
>&#09;&#09;`$fibonacci = $i;`
>&#09;&#09;`echo $fibonacci . "\n";`
>&#09;&#09;`}`
>&#09;&#09;`else {`
>&#09;&#09;`$fibonacci = $num1 + $num2;`
>&#09;&#09;`$num1 = $num2;`
>&#09;&#09;`$num2 = $fibonacci;`
>&#09;&#09;`echo $fibonacci . "\n";`
>&#09;&#09;`}`
>&#09;`}`
>`?>`