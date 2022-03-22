# Challenge 1: Find the Maximum Value
## Problem Statement
- Write a method named `findMaxVal()` to find the maximum integer value stored in an Array of any size.

> `<?php`<br/>
> &emsp;`//Returns maximum value from Array passed as parameter`<br/>
> &emsp;`function findMaxVal($arr)`<br/>
> &emsp;`{`<br/>
> &emsp;&emsp;`//write your code here`<br/>
> &emsp;&emsp;`$max = $arr[$i];`<br/>
> &emsp;&emsp;`for($i = 0; $i <= count($arr); $i++){`<br/>
> &emsp;&emsp;&emsp;`if ($arr[$i] > $max){`<br/>
> &emsp;&emsp;&emsp;&emsp;`$max = $arr[$i];`<br/>
> &emsp;&emsp;&emsp;`}`<br/>
> &emsp;&emsp;`}`<br/>
> &emsp;&emsp;`return $max;`<br/>
> &emsp;`}`<br/>
> &emsp;`$arr = array(2, 9, 6, 17, 15);`<br/>
> &emsp;`echo findMaxVal($arr);`<br/>
> `?>`<br/><br/>