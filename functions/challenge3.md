# Challenge 3: Fibonacci Sequence
## Problem Statement
- In this exercise, you have to write a recursive function fibonacci that takes an integer `range` as a parameter and returns the *nth* number from the Fibonacci Sequence where n is the value of the `range` variable.

> `<?php`
> &emsp;`function fibonacci($range){`
> &emsp;&emsp;`if($range == 0 || $range == 1){`
> &emsp;&emsp;&emsp;`return $range;`
> &emsp;&emsp;`}`
> &emsp;&emsp;`else {`
> &emsp;&emsp;&emsp;`return (fibonacci($range-1) + fibonacci($range-2));`	
> &emsp;&emsp;`}`
> &emsp;`}`
> &emsp;`echo fibonacci(7);`
> `?>`