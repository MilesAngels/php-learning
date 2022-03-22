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

> `<?php` <br/>
> &emsp;`function gpaPoint($grade){`<br/>
>   &emsp;&emsp;`switch($grade){`<br/>
>     &emsp;&emsp;&emsp;`case 'A+':`<br/>
>       &emsp;&emsp;&emsp;&emsp;`return 4;`<br/>
>       &emsp;&emsp;&emsp;&emsp;`break;`<br/>
>     &emsp;&emsp;&emsp;`case 'A':`<br/>
>       &emsp;&emsp;&emsp;&emsp;`return 4; `<br/>
>       &emsp;&emsp;&emsp;&emsp;`break;`<br/>
>     &emsp;&emsp;&emsp;`case 'A-':`<br/>
>       &emsp;&emsp;&emsp;&emsp;`return 3.7`; <br/>
>       &emsp;&emsp;&emsp;&emsp;`break;`<br/>
>     &emsp;&emsp;&emsp;`case 'B+':`<br/>
>       &emsp;&emsp;&emsp;&emsp;`return 3.3;` <br/>
>       &emsp;&emsp;&emsp;&emsp;`break;`<br/>
>     &emsp;&emsp;&emsp;`case 'B':`<br/>
>       &emsp;&emsp;&emsp;&emsp;`return 3;` <br/>
>       &emsp;&emsp;&emsp;&emsp;`break;`<br/>
>     &emsp;&emsp;&emsp;`case 'B-':`<br/>
>       &emsp;&emsp;&emsp;&emsp;`return 2.8;` <br/>
>       &emsp;&emsp;&emsp;&emsp;`break;`<br/>
>     &emsp;&emsp;&emsp;`case 'C+':`<br/>
>       &emsp;&emsp;&emsp;&emsp;`return 2.5;` <br/>
>       &emsp;&emsp;&emsp;&emsp;`break;`<br/>
>     &emsp;&emsp;&emsp;`case 'C':`<br/>
>       &emsp;&emsp;&emsp;&emsp;`return 2;` <br/>
>       &emsp;&emsp;&emsp;&emsp;`break;`<br/>
>     &emsp;&emsp;&emsp;`case 'C-':`<br/>
>       &emsp;&emsp;&emsp;&emsp;`return 1.8;` <br/>
>       &emsp;&emsp;&emsp;&emsp;`break;`<br/>
>     &emsp;&emsp;&emsp;`case 'D':`<br/>
>       &emsp;&emsp;&emsp;&emsp;`return 1.5;` <br/>
>       &emsp;&emsp;&emsp;&emsp;`break;`<br/>
>     &emsp;&emsp;&emsp;`case 'F':`<br/>
>       &emsp;&emsp;&emsp;&emsp;`return 0;` <br/>
>       &emsp;&emsp;&emsp;&emsp;`break;`<br/>
>     &emsp;&emsp;&emsp;`default:`<br/>
>       &emsp;&emsp;&emsp;&emsp;`return -1;`<br/>
>       &emsp;&emsp;&emsp;&emsp;`break;`<br/>
>   &emsp;&emsp;`}`<br/>
> &emsp;`}`<br/>
> `?> `