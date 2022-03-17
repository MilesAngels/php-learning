# Operators <br/>
## What are operators?
- An operator is something that takes one or more values (or expressions, in programming jargon) and yields another value (so that the construction itself becomes an expression). 
<br/>

### Types of Operators
- arithmetic operators
- comparison operators
- logical operators
- assignment operators
<br/><br/>

## Arithmetic Operators
- Used to perform basic arithmetic and are divided into two categories:
    1. Binary Operators
    2. Unary Operators

### Binary Operators
- Binary operators are the ones that take two values and perform an arithmetic operation on them. They are listed below:

 | Operator | Name | Example |
 |---|---|---|
 | + | Addition | \$a + \$b |
 | - | Subtraction | \$a - \$b |
 | * | Multiplication | \$a * \$b |
 | / | Division | \$a / \$b |
 | % | Modulus | \$a % \$b |


### Unary Operators
- Unary operators are the type of arithmetic operators that perform arithmetic on only one value.
<br/>

#### There are two types of unary operators
- Incrementing operator: `++`
- Decrementing operator: `--`
- They can either precede or succeed variables, resulting in different executions of the code. An example of this is shown below:
    - Example: 
        `<?php`<br/>
            `$i = 1;`
            `echo $i . "\n"; // Prints 1`<br/>
            `// Pre-increment operator increments $i by one, then returns $i`<br/>
            `echo ++$i . "\n"; // Prints 2`<br/>
            `// Pre-decrement operator decrements $i by one, then returns $i`<br/>
            `echo --$i . "\n"; // Prints 1`<br/>
            `// Post-increment operator returns $i, then increments $i by one`<br/>
            `echo $i++ . "\n"; // Prints 1 (but $i value is now 2)`<br/>
            `// Post-decrement operator returns $i, then decrements $i by one`<br/>
            `echo $i-- . "\n"; // Prints 2 (but $i value is now 1)`<br/>
        `?>`<br/><br/><br/>

## Precedence 
- Operator precedence determines which operator is performed first in an expression with more than one operators. Operator precedence in PHP is similar to that of regular arithmetic operators.
    - `*`,` /`, `%` operators have equal precedence.
    - `+` , `-` operators have equal precedence.
    - `*`, `/` , `%` have a higher precedence than `+` , `-`.

### Associativity 
- Associativity is used when two operators of the same precedence appear in an expression.

#### Left Associativity
- Left associativity occurs when an expression is evaluated from left to right. For example * and / have the same precedence and their associativity is left to right, so the expression

> 100 / 10 * 10 

- is treated as:

> (100 / 10) * 10

#### Right Associativity
- Right associativity occurs when an expression is evaluated from right to left. Like most programming languages, = and print in PHP have right associativity.
    - Example:<br/>
        `<?php` <br/>
            `echo "5 - 3 + 2 = " . (5 - 3 + 2); // 5-3+2 is treated as (5-3)+2`<br/>
            `echo "\n";`<br/>
            `echo "5 + 3 * 2 = " . (5 + 3 * 2); // 5+3*2 is treated as 5+(3*2)`<br/>
            `echo "\n";`<br/>
            `echo "15 / 3 * 5 = " . (15 / 3 * 5); // 15/3*5 is treated as (15/3)*5`<br/>
            `echo "\n";`<br/>
            `echo "42 + 7 % 2 = " . (42 + 7 % 2); // 42+7%2 is treated as 42+(7%2)`<br/>
        `?>` <br/><br/>

## Comparison Operators <br/>
### Basic Operators
 | Operator | Name | Example |
 |---|---|---|
 | == | Equal | `a==b` |
 | === | Identical | `a===b` |
 | != | Not Equal | `a!=b` |
 | !== | Not Identical | `a!==b` |
 | < | Less than | `a<b` |
 | > | Greater than | `a>b` |
 | <= | Less than equal to | `a<=b` |
 | >= | Greater than equal to | `a>=b` |


> Note: For basic equality testing, the equal operator `==` is used. For more comprehensive checks, use the identical operator `===`.

- Example:<br/>
    `<?php`<br/>
        `$a = 4;`<br/>
        `$b = '4';`<br/>
        `if ($a == $b)`<br/>
        `{`<br/>
            `echo 'a and b are equal'; // $b value is casted this will be printed`<br/>
        `}`<br/>
        `if ($a === $b)`<br/>
        `{ //try removing one = and see what happens`<br/>
            `echo 'a and b are identical'; // this won't be printed` <br/>
        `}`<br/>
    `?>`<br/><br/>

### Spaceship operator
- The spaceship operator (`<=>`) is a special kind of comparison operator. It
    - returns `-1` if first expression is lesser than the second expression.
    - returns `1` if the first expression is greater than the second expression.
    - returns `0` if the first expression is equal to the second expression.

- Example: <br/>
    `<?php`<br/>
        `// Integers`<br/>
        `echo (1<=>1) . ","; //prints 0`<br/>
        `echo (1<=>2) . ","; //prints -1`<br/>
        `echo (2<=>1); //prints 1`<br/>
        `echo "\n"; //skips to next line`<br/>
        `// Floats`<br/>
        `echo (1.5<=>1.5) . ","; //prints 0`<br/>
        `echo (1.5<=>2.5) . ","; //prints -1`<br/>
        `echo (2.5<=>1.5); //prints 1`<br/>
        `echo "\n"; //skips to next line`<br/>
        `// Strings`<br/>
        `echo ("a"<=>"a") . ","; //prints 0`<br/>
        `echo ("a"<=>"b") . ","; //prints -1`<br/>
        `echo ("b"<=>"a"); //prints 1`<br/>
    `?>`<br/><br/>

> Remember: Objects are not comparable, and doing so will result in undefined behavior.

## Logical Operators?
- Logical operators are used to combine conditional statements. This means that the program can take a decision based on multiple conditions. You will learn more about conditional statements later. But for now, suffice it to say, that conditional statements are those that can either be true or false.

### Types of Logical Operator
- There are two logical operators:
    - `&&` or and
    - `||` or or

#### The AND Operator
- The `and` or `&&` operator returns `true` if all the statements are `true` and `false` if one or more statements are `false`. Say we have two statements `a` and `b`. The following table illustrates this behavior.

 | a | b | `a&&b` or `a and b` |
 |---|---|---|
 | true | true | true |
 | true | false | false |
 | false | true | false |
 | false | false | false |

- Example: <br/> 
    `<?php`
        `$x = 5;`
        `$y = 4;`
        `$z = 2;`
        `if ($x > $y && $x > $z) echo "x is greater than y and z\n";`
        `if ($z < $y and $z < $x) echo "z is smaller than y and z\n";`
    `?>`

#### The OR operator
- The `or` operator returns `true` if one or more of the conditional statements are `true` and `false` if all the conditions are `false`. The following table illustrates this behavior.

 | a | b | `a&&b` or `a and b` |
 |---|---|---|
 | true | true | true |
 | true | false | false |
 | false | true | false |
 | false | false | false |


- Example: <br/>
    `<?php`<br/>
        `$x = true;`<br/>
        `$y = false;`<br/>
        `$z = true;`<br/>
        `echo ($x || $y);`<br/>
    `?>`<br/><br/>

    <br/>
    `<?php`<br/>
        `$x = 5;`<br/>
        `$y = 6;`<br/>
        `$z = 2;`<br/>
        `if ($x > $y || $x > $z) echo "x is either greater than y or z";`<br/>
    `?>`<br/><br/>

> Note: The && and || operators have higher precedence than and and or respectively. See table below:
> Since the precedence of `or` and `and` is lower, the `=` operator is executed first.
