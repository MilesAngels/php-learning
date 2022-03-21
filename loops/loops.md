# Introduction to Loops

## What are Loops? 
- Loops allow a programmer to execute the same block of code repeatedly instead of re-writing code that needs to be executed multiple times.
    - Types of Loops
        - while loop
        - do...while loop
        - for loop
        - foreach loop

## While Loops
- The while loop is really the only necessary repetition construct. The while loop consists of a condition and while that condition is true, a set of statements is executed repeatedly. 
- Example: <br/>
    `<?php`<br/>
        `$x = 4;`<br/>
        `$y = 0;`<br/>
        `while ($y <= 10)`<br/>
        `{ // the while loop will run till y<=10 condition is being met`<br/>
            `$y += $x;`<br/>
            `$x += 1;`<br/>
            `echo "Value of y: $y ";`<br/>
            `echo "Value of x: $x\n";`<br/>
        `} //the loop will iterate 3 times`<br/>
        `echo "the value of x is: $x\n";`<br/>
        `echo "the value of y is: $y\n";`<br/>
    `?>`<br/><br/>

>**Infinite Loops**
> - if the while loop's conditional statement looked like this instead: 
> `while ( $y <= 10 ) { //since y is not being changed inside the while loop you will get stuck `
>       `$x += 1;        // in an infinte loop as the condiiton will always be met` 
>  `}`
>   `$y += $x;`