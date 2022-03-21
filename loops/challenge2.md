# Challenge 2: Fibonacci Sequence up to n Number Of Terms
## Problem Statement
- In this exercise, you have to write Fibonacci Sequence of a given number.
    - You have to print the sequence up to the given range.
    - There is a string variable ans given in which you have to store all the Fibonacci values computed up to the given range by appending them.
        - Here’s a link showing how you can add values to a string.

>`<?php`<br/>
>&emsp;`$range = 6; //this will be the range of the fibonacci sequence`<br/>
>&emsp;`//$ans = ""; //this will be the output`<br/>
>&emsp;`$num1 = 0; // 1st value in the fibonacci sequence`<br/>
>&emsp;`$num2 = 1; //2nd value in the fibonacci sequence`<br/>
>&emsp;`$fibonacci = 0;`<br/>
>&emsp;`echo "Fibonacci Series upto $range Terms \n";`<br/>
>&emsp;`for($i = 0; $i < $range; $i++) {`<br/>
>&emsp;&emsp;`if($i <= 1){`<br/>
>&emsp;&emsp;`$fibonacci = $i;`<br/>
>&emsp;&emsp;`echo $fibonacci . "\n";`<br/>
>&emsp;&emsp;`}`<br/>
>&emsp;&emsp;`else {`<br/>
>&emsp;&emsp;`$fibonacci = $num1 + $num2;`<br/>
>&emsp;&emsp;`$num1 = $num2;`<br/>
>&emsp;&emsp;`$num2 = $fibonacci;`<br/>
>&emsp;&emsp;`echo $fibonacci . "\n";`<br/>
>&emsp;&emsp;`}`<br/>
>&emsp;`}`<br/>
>`?>`<br/>