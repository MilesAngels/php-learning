# if-else Statements

## Branches in PHP
- Programming in general often requires a decision or a branch within the code to account for how the code operates under different inputs or conditions. One way of creating these branches is through using the if-else statement

## if-else
- Example: check whether the value of variable a is greater than or less than the value of variable b.<br/>
    `<?php`<br/>
        `$a = 50; //change the value of "a" so its less than b in order to execute the else statement`<br/>
        `$b = 15;`<br/>
        `if ($a > $b)`<br/>
        `{`<br/>
            `//this code is executed only if $a is greater than $b`<br/>
            `echo "a is greater than b";`<br/>
        `}`<br/>
        `else`<br/>
        `{`<br/>
            `//this code is executed if the preceding "if" condition evaluated to false`<br/>
            `echo "a is less than b";`<br/>
        `}`<br/>
    `?>`<br/><br/>

## Nested-if
- Example: <br/>
    `if(condition1){`<br/>
        `//execution statement(s) `<br/>
        `if(condition2){`<br/>
            `//execution statement(s)`<br/>
        `}//end of inner if`<br/>
        `else{`<br/>
            `//execution statement(s)`<br/>
        `}//end  of inner else`<br/>
    `}//end ofouter if`<br/>
    `else{`<br/>
    `//execution statement(s)` <br/>
    `}//end ofouter else`<br/><br/>


# if-elseif-else Statement

## Else-ifs 
- Else-ifs are the complex nested form of if-else block. They are used when you have to check multiple conditions and there’s a different action that needs to be performed corresponding to every condition. 

- Syntax
    - Example: <br/>
        `<?php`<br/>
            `$score = 50; //change the value of score to see other results`<br/>
            `if ($score > 100)`<br/>
            `{ // If score is greater than 100`<br/>
                `echo "Error: the score is greater than 100!\n";`<br/>
            `}`<br/>
            `else if ($score < 0)`<br/>
            `{ // Else If score is less than 0`<br/>
                `echo "Error: the score is less than 0!\n";`<br/>
            `}`<br/>
            `else if ($score >= 50)`<br/>
            `{ // Else if score is greater or equal to 50`<br/>
                `echo "Pass!\n";`<br/>
            `}`<br/>
            `else`<br/>
            `{ // If none above, then score must be between 0 and 49`<br/>
                `echo "Fail!\n";`<br/>
            `}`<br/>
        `?>`<br/><br/>

# Switch Statements

## Switch Case Construct
- Typically this is required when based on different values of a particular expression, different actions need to be performed. The basic construct of a switch case looks as follows:
    `switch (expression)`<br/>
    `{`<br/>
    `case constant-expression: `<br/>
        `statement; //statement(s) execute if constant-expression is true`<br/>
        `break; //exit the switch block `<br/>
    `default: //the code inside default is run when no other cases match`<br/>
        `statement;`<br/>
        `break;`<br/>
    `}`<br/><br/>
- Example: <br/>
    `<?php`<br/>
        `$x = 2; //change value of x to see output for different cases`<br/>
        `switch ($x) {`<br/>
        `case 1: //is x=1?`<br/>
            `echo "Your value for case 1 is $x";`<br/>
            `break;`<br/>
        `case 2: //is x=2?`<br/>
            `echo "Your value for case 2 is $x";`<br/>
            `break;`<br/>
        `default: //executed if neither case 1 nor case 2 are executed`<br/>
            `echo "Your value in default case is $x";`<br/>
            `break;`<br/>
        `}`<br/>
    `?>` <br/><br/>

# Ternary Operator

- The ternary operator is a comparison operator that evaluates something based on a condition being true or not.
- It is a shorthand syntax for if-else statement.
- It allows to quickly test a condition and often replaces a multi-line if statement, making your code more compact.
- Example: <br/>
    `<?php`<br/>
        `$a = 1; //Change values of $a and $b to change output of the code.`<br/>
        `$b = 2;`<br/>
        `echo ($a > $b) ? "a is greater than b" : "a is NOT greater than b";`<br/>
    `?>`<br/><br/>

