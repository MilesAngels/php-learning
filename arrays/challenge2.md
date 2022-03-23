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
> `?>`<br/>

<br/><br/>

- My Own Solution<br/>
> `<?php`<br/>
> &emsp;`function printMat($n) {`<br/>
> &emsp;`//write the code for making and printing the matrix here`<br/>
> &emsp;`//use can use \n to move numers to next line in the matrix`<br/>
> &emsp;`//use " " to add space between numbers in matrix`<br/>
> &emsp;`//echo "not complete";//comment out this line when you start writing code`<br/>
> &emsp;&emsp;`for($i = 0; $i <= count($n); $i++){//iterates through the array index`<br/>
> &emsp;&emsp;&emsp;`for($j = 0; $j <= count($n)-1; $j++){//iterates through the array within the array and prints them`<br/>
> &emsp;&emsp;&emsp;&emsp;`echo $n[$i][$j] . " ";`<br/>
> &emsp;&emsp;&emsp;&emsp;`if ($j === count($n[$j])-1){//if the inner array is 1 less than the total count then put a newline.`<br/>
> &emsp;&emsp;&emsp;&emsp;&emsp;`echo PHP_EOL;`<br/>
> &emsp;&emsp;&emsp;&emsp;`}`	<br/>	
> &emsp;&emsp;&emsp;`}`<br/>
> &emsp;&emsp;`}`<br/>
> &emsp;`}`<br/>
> &emsp;`$num = array(array(0,1,2), array(3,4,5), array(6,7,8));`<br/>
> &emsp;`echo printMat($num)`<br/>
> `?>`<br/><br/>