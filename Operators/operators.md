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
<br/>
 | Operator |    Function    | Example   |
 
 |----------|----------------|-----------|
 |     +    |    Addition    | \$a + \$b |
 |     -    |   Subtraction  | \$a - \$b |
 |     *    | Multiplication | \$a * \$b |
 |     /    |    Division    | \$a / \$b |
 |     %    |     Modulus    | \$a % \$b |
<br/><br/><br/>

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
    - Example:
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
