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
     for (initialization; condition; change) { <br/>
        statement / code block; <br/>
    }<br/><br/>
- Example: <br/>
    `<?php`<br/>
        `for ($i = 0;$i < 10;$i++)`<br/>
        `{`<br/>
            `echo "value of i is: $i\n";`<br/>
        `}`<br/>
    `?>`<br/><br/>
- Other ways to write a for loop
    - Example 1:<br/>
        `<?php`<br/>
           ` $i = 0;`<br/>
            `for (;$i < 10;$i++)`<br/>
            `{ //initialization can also be done outside loop`<br/>
                `echo "value of i is: $i\n";`<br/>
            `}`<br/>
        `?>`<br/>
    - Example 2: <br/>
        `<?php`<br/>
            `$i = 0;`<br/>
            `for (;$i < 10;)`<br/>
            `{ //initialization can also be done outside loop. Note the semicolon is compulsory`<br/>
                `echo "value of i is: $i \n";`<br/>
                `$i++; //the increment of loop control variable can also be done separately`<br/>  
            `}`<br/>
        `?>`<br/><br/>

> **Nested For Loops**
> - It is possible to nest for loops. Nesting means including one for loop in another​ for loop.
> - The syntax for a nested for loop is as follows:<br/>
> `for (expression for initialization ; expression for testing ; expression for updating ) {`<br/>
>    `for (expression for initialization ; expression for testing ; expression for updating) {`<br/>
>        `//body`<br/>
>    `}`<br/>
>    `//body`<br/>
>  `}`<br/> 

## Foreach Loop
- The `foreach` statement is similar to the `for` statement in that both allow code to iterate over the items of collections, but the `foreach` statement lacks an iteration index, so it works even with collections that lack indices altogether.
- Syntax: <br/>
    `foreach(x as y) {`<br/>
        `statement;`<br/>
    `}`<br/><br/>
- Example: <br/>
    `<?php`<br/> 
    `$itemsToWrite = array('Alpha', 'Bravo', 'Charlie'); //an array of strings `<br/>
    `foreach($itemsToWrite as $item){ //iterating through each element of array itemsToWrite`<br/>
        `echo "$item\n"; //displaying each element of array in console`<br/>
    `}`<br/>
    `?>`<br/><br/>

## Infinite Loops
- An infinite loop refers to a loop, which under certain valid (or at least plausible) input, will never exit.  
