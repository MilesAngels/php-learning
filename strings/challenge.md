# Challenge: Check Substring
## Problem Statement
- In this challenge, you have to write code that checks if a string contains a specific string. Your code should return 1 if it does else return 0.

> `<?php` <br/>
> &emsp;`function stringCheck($str1,$str2){`<br/>
> &emsp;&emsp;`if (strpos($str1, $str2) !== false){`<br/>
> &emsp;&emsp;&emsp;`return 1;`<br/>
> &emsp;&emsp;`}`<br/>
> &emsp;&emsp;`else{`<br/>
> &emsp;&emsp;&emsp;`return 0;`<br/>
> &emsp;&emsp;`}`<br/>
> &emsp;`}`<br/>
> &emsp;`echo stringCheck("The quick brown fox jumps over the lazy dog.", "The");`<br/>
> `?>`<br/>