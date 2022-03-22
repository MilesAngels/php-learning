# Challenge 2: Letter Grade to GPA
## Problem Statement
- Write a method called gpaPoint that takes in a string value and returns the correct decimal GPA point, with respect to the scale given below:
    - A+: 4
    - A: 4
    - A-: 3.7
    - B+: 3.3
    - B: 3
    - B-: 2.8
    - C+: 2.5
    - C: 2
    - C-: 1.8
    - D: 1.5
    - F: 0
    - If any other grade is given, simply return a -1.

> `<?php` 
> &emsp;`function gpaPoint($grade){`
>   &emsp;&emsp;`switch($grade){`
>     &emsp;&emsp;&emsp;`case 'A+':`
>       &emsp;&emsp;&emsp;&emsp;`return 4;`
>       &emsp;&emsp;&emsp;&emsp;`break;`
>     &emsp;&emsp;&emsp;`case 'A':`
>       &emsp;&emsp;&emsp;&emsp;`return 4; `
>       &emsp;&emsp;&emsp;&emsp;`break;`
>     &emsp;&emsp;&emsp;`case 'A-':`
>       &emsp;&emsp;&emsp;&emsp;`return 3.7`; 
>       &emsp;&emsp;&emsp;&emsp;`break;`
>     &emsp;&emsp;&emsp;`case 'B+':`
>       &emsp;&emsp;&emsp;&emsp;`return 3.3;` 
>       &emsp;&emsp;&emsp;&emsp;`break;`
>     &emsp;&emsp;&emsp;`case 'B':`
>       &emsp;&emsp;&emsp;&emsp;`return 3;` 
>       &emsp;&emsp;&emsp;&emsp;`break;`
>     &emsp;&emsp;&emsp;`case 'B-':`
>       &emsp;&emsp;&emsp;&emsp;`return 2.8;` 
>       &emsp;&emsp;&emsp;&emsp;`break;`
>     &emsp;&emsp;&emsp;`case 'C+':`
>       &emsp;&emsp;&emsp;&emsp;`return 2.5;` 
>       &emsp;&emsp;&emsp;&emsp;`break;`
>     &emsp;&emsp;&emsp;`case 'C':`
>       &emsp;&emsp;&emsp;&emsp;`return 2;` 
>       &emsp;&emsp;&emsp;&emsp;`break;`
>     &emsp;&emsp;&emsp;`case 'C-':`
>       &emsp;&emsp;&emsp;&emsp;`return 1.8;` 
>       &emsp;&emsp;&emsp;&emsp;`break;`
>     &emsp;&emsp;&emsp;`case 'D':`
>       &emsp;&emsp;&emsp;&emsp;`return 1.5;` 
>       &emsp;&emsp;&emsp;&emsp;`break;`
>     &emsp;&emsp;&emsp;`case 'F':`
>       &emsp;&emsp;&emsp;&emsp;`return 0;` 
>       &emsp;&emsp;&emsp;&emsp;`break;`
>     &emsp;&emsp;&emsp;`default:`
>       &emsp;&emsp;&emsp;&emsp;`return -1;`
>       &emsp;&emsp;&emsp;&emsp;`break;`
>   &emsp;&emsp;`}`
> &emsp;`}`
> ?> 