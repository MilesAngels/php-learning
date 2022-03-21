# Challenge 2: Fibonacci Sequence up to n Number Of Terms
## Problem Statement
- In this exercise, you have to write Fibonacci Sequence of a given number.
    - You have to print the sequence up to the given range.
    - There is a string variable ans given in which you have to store all the Fibonacci values computed up to the given range by appending them.
        - Here’s a link showing how you can add values to a string.

>`<?php`<br/>
>&#09;`$range = 6; //this will be the range of the fibonacci sequence`<br/>
>&#09;`//$ans = ""; //this will be the output`<br/>
>&#09;`$num1 = 0; // 1st value in the fibonacci sequence`<br/>
>&#09;`$num2 = 1; //2nd value in the fibonacci sequence`<br/>
>&#09;`$fibonacci = 0;`<br/>
>&#09;`echo "Fibonacci Series upto $range Terms \n";`<br/>
>&#09;`for($i = 0; $i < $range; $i++) {`<br/>
>&#09;&#09;`if($i <= 1){`<br/>
>&#09;&#09;`$fibonacci = $i;`<br/>
>&#09;&#09;`echo $fibonacci . "\n";`<br/>
>&#09;&#09;`}`<br/>
>&#09;&#09;`else {`<br/>
>&#09;&#09;`$fibonacci = $num1 + $num2;`<br/>
>&#09;&#09;`$num1 = $num2;`<br/>
>&#09;&#09;`$num2 = $fibonacci;`<br/>
>&#09;&#09;`echo $fibonacci . "\n";`<br/>
>&#09;&#09;`}`<br/>
>&#09;`}`<br/>
>`?>`<br/>