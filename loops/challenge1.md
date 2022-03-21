# Challenge 1: Multiplication Table of a Number
## Problem Statement
- Write a code which will
    - Print the multiplication table of a number num up to 10.
    - You have to use while loop for solving this problem.
    - Your code should return the string ans with all the values computed from multiplication appended in that string.

>`<?php`<br/>	
>>`$num = 5;`
>>`$i = 10; // end of loop flag`
>	`$k=1; // start of loop `
>	`$ans = ""; //total` 
>	`while($i>0)`
>		//while i is greater than 0 then keep going
>	{
>	  $answer = $num*$k; 
>	  echo "$num x $k  = $answer\n";
>		//strval() is a function that returns the string value of a variable
>	  $ans .=  strval($answer)." ";
>	  $k++;
>	  $i--;
>	}
>?>