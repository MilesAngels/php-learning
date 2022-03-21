# Introduction to Loops

## What are Loops? 
- Loops allow a programmer to execute the same block of code repeatedly instead of re-writing code that needs to be executed multiple times.
    - Types of Loops
        - while loop
        - do...while loop
        - for loop
        - foreach loop

## While Loops
- The while loop is really the only necessary repetition construct. The while loop consists of a condition and `while` that condition is true, a set of statements is executed repeatedly. 
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
> - if the while loop's conditional statement looked like this instead: <br/>
> `while ( $y <= 10 ) { //since y is not being changed inside the while loop you will get stuck `<br/>
>       `$x += 1;        // in an infinte loop as the condiiton will always be met` <br/>
>  `}`<br/>
>   `$y += $x;`
<br/><br/>

## Do...while Loop
- The **do…while** loop is nearly identical to the `while` loop, but instead of checking the conditional statement before the loop starts, the **do…while** loop checks the conditional statement after the first run, before moving onto another iteration.
> The while loop runs the code inside it if and only if the condition inside the parenthesis is true. The do...while, however, runs the loop at least once before checking the conditional.
> Be careful of infinite loops.

- Example: <br/>
    `<?php`<br/>
        `$number = 5;`<br/>
        `do`<br/>
        `{`<br/>
            `echo "Value of number is: $number\n";`<br/>
            `$number++;`<br/>
        `}`<br/>
        `while ($number <= 9); // the contition is being checked after the first run`<br/>
    `?>`<br/><br/>

- We can use a **do...while** loop if you need your loop to execute at least once. 

## For Loop
- A for loop can also be used for doing things a certain amount of time. It’s like a while loop but the increment is included with the condition.
- Syntax:<br/>
     for (<mark style="background-color: yellow">initialization</mark>; condition; change) { <br/>
        statement / code block; <br/>
    }<br/>