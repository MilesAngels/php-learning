# Challenge 3: Pyramid Printing By Using For Loop
## Problem Statement#
- Write code which prints half a pyramid of the alphabet a.
    - The code takes an integer variable rows as input and prints the pyramid with that number of rows displaying a.

>`<?php`<br/>
>&emsp;`$rows = 5;//rows we need to construct`<br/>
>&emsp;`for ($i = 0; $i <= $rows; $i++){//building rows`<br/>
>&emsp;&emsp;`for ($j = 1; $j <= $i; $j++){//building columns`<br/>
>&emsp;&emsp;&emsp;`echo "a ";`<br/>
>&emsp;&emsp;`}`<br/>
>&emsp;&emsp;`echo "\n";`<br/>
>&emsp;`}`<br/>
>`?>`<br/>