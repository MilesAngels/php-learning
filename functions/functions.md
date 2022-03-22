# Functions
- A function is a block of code that is written in order to perform a specific task.
    - Types of Functions
        - Built-in functions
        - User-defined functions

## Built-in functions
- These functions are pre-defined and just need to be called. Here are a few [built-in functions](https://www.php.net/manual/en/indexes.functions.php)

## User-defined functions
- These functions can be written such that they would perform the required task wherever necessary once they’re called.
- Custom functions
- Example: <br/>
`<?php`<br/>
&emsp;`function exampleFunc() //function that outputs some text`<br/>
&emsp;`{`<br/>
&emsp;&emsp;`echo "This is a user-defined function";`<br/>
&emsp;`}`<br/>
&emsp;`// Calling the function`<br/>
&emsp;`exampleFunc();`<br/>
`?>`<br/><br/>

### Passing Arguments in Functions
- *Parameters* are passed in the parentheses of the functions. They are used to hold values during runtime of a function. A user can pass multiple parameters into a function, each one separated by a comma.
- The parameters of a function accept values passed to them when that function is called. The values passed are referred to as **arguments** of a function.
- Example: <br/>
`<?php`<br/>
&emsp;`//function with two parameters`<br/>
&emsp;`function myFunction($num1, $num2)`<br/>
&emsp;`{`<br/>
&emsp;&emsp;`echo "The value assigned to num1 is $num1\n";`<br/>
&emsp;&emsp;`echo "The value assigned to num2 is $num2";`<br/>
&emsp;`}`<br/>
&emsp;`//calling function and passing arguments to it`<br/>
&emsp;`myFunction(3, 4);`<br/>
`?>`<br/><br/>

>- PHP allows us to pass arguments into a function in two ways:
>    - Pass by Value
>    - Pass by Reference

### Pass by Value
- On passing arguments using pass by value, the value of the argument gets changed within a function, but the original value outside the function remains unchanged. 
- That means a duplicate of the original value is passed as an argument.(Shallow copy)

- Example: Cube of a Number <br/>
`<?php`<br/>
&emsp;`function cube($num1)`<br/>
&emsp;`{ //num1 parameter passed by value here`<br/>
&emsp;&emsp;`return $num1 * $num1 * $num1; //cube of num1 returned`  <br/>
&emsp;`}`<br/>
&emsp;`$answer = cube(3); //function cube called with 3 passed as the argument`<br/>
&emsp;`echo $answer;`<br/>
`?>`<br/><br/>

- Example: Swap Numbers<br/>
`<?php`<br/>
&emsp;`function swap($arg1, $arg2)`<br/>
&emsp;`{ //parameters num1 and num2 passed using pass by value method`<br/>
&emsp;&emsp;`$temp = $arg2; //creating a variable temp and setting equal to arg2`<br/>
&emsp;&emsp;`$arg2 = $arg1; //setting the value of arg2 equal to arg1`<br/>
&emsp;&emsp;`$arg1 = $temp; //setting the value of arg1 equal to temp which is equal to arg2`<br/>
&emsp;`}`<br/>
&emsp;`$num1 = 4;`<br/>
&emsp;`$num2 = 5;`<br/>
&emsp;`// Have a careful look at this function call`<br/>
&emsp;`swap($num1, $num2);`<br/>
&emsp;`echo "num1 is: $num1\n";`<br/>
&emsp;`echo "num2 is: $num2";`<br/>
`?>`<br/><br/>

### Pass by Reference
- When passing arguments by pass by reference, the original value is passed. Therefore, the original value gets altered. 
- In pass by reference, we actually pass the value using ampersand sign `&`. **The additional `&` is very important: it tells the compiler that the data is a reference to the value rather than simply the value itself.**

- Example: Swap Numbers<br/>
`<?php`<br/>
&emsp;`function swap(&$arg1, &$arg2)`<br/>
&emsp;`{ //parameters num1 and num2 passed using pass by value method`<br/>
&emsp;&emsp;`$temp = $arg2; //creating a variable temp and setting equal to arg2`<br/>
&emsp;&emsp;`$arg2 = $arg1; //setting the value of arg2 equal to arg1`<br/>
&emsp;&emsp;`$arg1 = $temp; //setting the value of arg1 equal to temp which is equal to arg2`<br/>
&emsp;`}`<br/>
&emsp;`$num1 = 4;`<br/>
&emsp;`$num2 = 5;`<br/>
&emsp;`// Have a careful look at this function call`<br/>
&emsp;`swap($num1, $num2);`<br/>
&emsp;`echo "num1 is: $num1\n";`<br/>
&emsp;`echo "num2 is: $num2";`<br/>
`?>`<br/><br/>
> This example works because we referenced the variables that we passed into the function which made it possible to change the original value of both variables.

## Variable Scope 
- The scope of a variable refers to the variables's visibility, i.e., which part of the program can access that variable.
- Types of Variables
    - local variables
    - global variables

### Local Variables
- Variables that are defined within a function. (local scope)
- These variables cannot be accessed outside of the function they are declared in.
- Example: <br/>
    `<?php`<br/>
    &emsp;`function foo()`<br/>
    &emsp;`{`<br/>
    &emsp;&emsp;`$number = 10;`<br/>
    &emsp;&emsp;`echo $number;`<br/>
    &emsp;`}`<br/>
    &emsp;`foo(); //Will print 10 because text defined inside function is a local variable`<br/>
    `?>`<br/><br/>

### Global Variable
- Variables that are defined outside of a function.
- Accessible to any part of the program
- To modify a global variable within a function, we need to use the keyword global followed by the name of the variable. 
    - Example:<br/>
    `<?php`<br/>
    &emsp;`$num1 = 5;`<br/>
    &emsp;`$num2 = 2;`<br/>
    &emsp;`function multiply(){`<br/>
    &emsp;&emsp;`global $num1; // Accessing global variables from function scope requires this explicit statement`<br/>
    &emsp;&emsp;`global $num2;`<br/>
    &emsp;&emsp;`$answer = $num1*$num2;`<br/>
    &emsp;&emsp;`return $answer;`<br/>
    &emsp;`}`<br/>
    &emsp;`// When in the global scope, regular global variables can be used`<br/>
    &emsp;`// without explicitly stating 'global $variable;'`<br/>
    &emsp;`echo "num1 is: $num1\n";`<br/>
    &emsp;`echo "num2 is: $num2\n";`<br/>
    &emsp;`echo multiply();`<br/>
    `?>`<br/><br/>

> *Using Variable Variables for Function Calls*
> - Example: <br/>
> `<?php`<br/>
> &emsp;`function sum($x, $y)`<br/>
> &emsp;`{`<br/>
> &emsp;&emsp;`return $x + $y;`<br/>
> &emsp;`}`<br/>
> &emsp;`$funcName = 'sum'; //we set the variable funcName to sum which means that the function named sum will equal to the newly declared variable`<br/>
> &emsp;`echo $funcName(2, 4); // outputs 6;`<br/>
> `?>`<br/>