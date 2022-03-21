# Challenge 1: Multiplication Table of a Number
## Problem Statement
- Write a code which will
    - Print the multiplication table of a number num up to 10.
    - You have to use while loop for solving this problem.
    - Your code should return the string ans with all the values computed from multiplication appended in that string.

>`<?php`<br/>	
>&nbsp;`$num = 5;//base number you wish to multiply`<br/>
>&nbsp;`$i = 10; //end of loop flag`<br/>
>&nbsp;`$k=1; //initialize loop`<br/>
>&nbsp;`$ans = ""; //product` <br/>
>&nbsp;`while($i>0) //while i is greater than 0 then keep going`<br/>
>&nbsp;`{`<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;` $answer = $num*$k;//declare a new variable and make it equal to the base num and loop iteration `<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;` echo "$num x $k  = $answer\n";//print out the table`<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;` //strval() is a function that returns the string value of a variable`<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;` $ans .=  strval($answer)." ";`<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;` $k++;`<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;` $i--;`<br/>
>&nbsp;`}`<br/>
>`?>`<br/>