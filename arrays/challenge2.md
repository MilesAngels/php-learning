# Challenge 2: Print a Matrix
## Problem Statement
- Print a two-dimensional array of size n x n as shown below in the form of a matrix.<br/>

> `<?php`<br/>
> &emsp;`function printMat($n)`<br/>
> &emsp;`{`<br/>
> &emsp;&emsp;`$arr = array();`<br/>
> &emsp;&emsp;`for ($i = 0;$i < $n;$i++)`<br/>
> &emsp;&emsp;`{`<br/>
> &emsp;&emsp;&emsp;`for ($j = 0;$j < $n;$j++)`<br/>
> &emsp;&emsp;&emsp;`{`<br/>
> &emsp;&emsp;&emsp;&emsp;`if ($i == $j)`<br/>
> &emsp;&emsp;&emsp;&emsp;`{ // if row=column=> fill the matrix with 0`<br/>
> &emsp;&emsp;&emsp;&emsp;&emsp;`$arr[$i][$j] = 0;`<br/>
> &emsp;&emsp;&emsp;&emsp;`}`<br/>
> &emsp;&emsp;&emsp;&emsp;`else if ($i > $j)`<br/>
> &emsp;&emsp;&emsp;&emsp;`{ // if row>columns=> fill matrix with -1`<br/>
> &emsp;&emsp;&emsp;&emsp;&emsp;`$arr[$i][$j] = - 1;`<br/>
> &emsp;&emsp;&emsp;&emsp;`}`<br/>
> &emsp;&emsp;&emsp;&emsp;`else`<br/>
> &emsp;&emsp;&emsp;&emsp;`{ // if row<columns=> fill matrix with 1`<br/>
> &emsp;&emsp;&emsp;&emsp;&emsp;`$arr[$i][$j] = 1;`<br/>
> &emsp;&emsp;&emsp;&emsp;`}`<br/>
> &emsp;&emsp;&emsp;`}`<br/>
> &emsp;&emsp;`}`<br/>
> &emsp;&emsp;`for ($i = 0;$i < $n;$i++)`<br/>
> &emsp;&emsp;`{ // printing the array`<br/>
> &emsp;&emsp;&emsp;`for ($j = 0;$j < $n;$j++)`<br/>
> &emsp;&emsp;&emsp;`{`<br/>
> &emsp;&emsp;&emsp;&emsp;`echo $arr[$i][$j] . " ";`<br/>
> &emsp;&emsp;&emsp;`}`<br/>
> &emsp;&emsp;`echo PHP_EOL;`<br/>
> &emsp;&emsp;`}`<br/>
> &emsp;`}`<br/>
> `?>`<br/><br/>