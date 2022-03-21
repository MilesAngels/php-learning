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
`?>`<br/>