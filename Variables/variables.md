# Variables and Data Types<br/>

## Variables
- A variable in any programming language is a named piece of computer memory, containing some information inside.
- You can declare a variable in PHP using the `$` sign followed by the variable name.
    - Example: `$name`

`<?php`<br/>
    `$str = "I will be back by";`<br/>
    `$num = 5;`<br/><br/>
    `echo $str;`<br/>
    `echo " "; // Output: I will be back by`<br/>
    `echo $num; // Output: 5`<br/>
`?>`<br/><br/><br/>

## Data Types
- PHP does not have explicit type definitions, but the type of variable is determined by the type of the value that it is assigned, or by the type that it is cast to.

### Null
- It can be assigned to anut variable. It represents a variable with no value.
    - Example: `<?php $foo = null;?>`
- The value will be undefined or void if it is used.
<br/><br/>

### Boolean
- This is the simplest data type with only two possible values: `true` and `false`<br/>
    - Example: `<?php`<br/>
                    `$foo = null;`<br/>
                `?>`<br/>
- Can be used to control the flow of code. 
    - Example: `<?php`<br/>
                    `// ignore the if and else for now. We'll study more`<br/> `about them later.`<br/>
                    `$foo = true;`<br/>
                    `if ($foo) {`<br/>
                        `echo "true";`<br/>
                    `}` <br/>
                    `else {`<br/>
                        `echo "false";`<br/>
                    `}`<br/>
                `?>`<br/><br/><br/>

### Integer
- An integer is a positive or negative number. 
    - Example: `<?php`<br/>
                    `$negative = -3; // negative`
                    `$zero = 0; // zero (can also be null or false (as boolean)`<br/>
                    `$positive = 123; // positive decimal`<br/>
                    `$zeroPos = 0123; //0 prefix is used to specify octal - octal value = 83 decimal`<br/>
                    `$hex = 0xAB; //0x prefix is used to specify hexadecimal - hexadecimal value = 171 decimal`<br/>
                    `$bin = 0b1010; // 0b prefix is used to specify binary - binary value = 10 decimal`<br/>
                    `var_dump($negative, $zero, $positive, $zeroPos, $hex, $bin); `<br/>
                `?>`<br/><br/><br/>

### Float
- Floating point numbers, "doubles" or simply called "floats" are decimal numbers.
    - Example: `<?php`<br/>
                    `$foo1 = 1.23;`<br/>
                    `$foo2 = 10.0;`<br/>
                    `$bar1 = -INF; // -INF refers to negative infinity`<br/>
                    `$bar2 = NAN; // NAN stands for 'Not a Number'`<br/>
                    `var_dump($foo1,$foo2,$bar1,$bar2);`<br/>
                `?>`<br/><br/><br/>

### Array
- An array is like a list of values. The simplest form of an array is indexed by an integer, and ordered by the index, with the first element lying at index 0.
    - Example: `<?php`<br/>
                    `$foo = array(1, 2, 3); // An array of integers created using array fucntion`<br/>
                   ` $bar = ["A", true, 123 => 5]; // Short array syntax, PHP 5.4+`<br/>
                    `echo $bar[0]; // Returns "A"`<br/>
                    `echo "\n";`<br/>
                    `echo $bar[1]; // Returns 1 for true`<br/>
                    `echo "\n";`<br/>
                    `echo $bar[123]; // Returns 5`<br/>
                    `// echo $bar[1234]; // uncommenting this line will give an error because 1234 is inaccessable`<br/>
                `?>`<br/><br/>
- Arrays can also associate a key other than an integer index to a value. In PHP, all arrays are associative arrays behind the scenes, but when we refer to an associative array explicitly, we usually mean one that contains one or more keys that aren’t integers.
    - Example:<br/><br/>
            `<?php`<br/>
            `$array = array();`<br/>
            `$array["foo"] = "bar";`<br/>
            `$array["bar"] = "quux";`<br/>
            `$array[42] = "hello";`<br/>
            `echo $array["foo"]; // Outputs "bar"`<br/>
            `echo "\n";`<br/>
            `echo $array["bar"]; // Outputs "quux"`<br/>
            `echo "\n";`<br/>
            `echo $array[42]; // Outputs "hello"`<br/>
            `?>`<br/><br/><br/>


### String
- A string is like an array of characters. Like an array, a string can be indexed to return its individual characters:
    - Example: <br/>
        `<?php`
        `$foo = "I am a string";`
        `echo $foo; // outputs "I am a string"`
        `echo "\n";`
        `echo $foo[3]; // Prints 'm', the third character of the string in $foo.`
        `?>`<br/><br/>

## *Variable* Variables
- The name of a variable can be stored in another variable, allowing it to be accessed dynamically. Such variables are known as variable variables.
- To turn a variable into a *variable* variable, we just need to put an extra `$` sign in front of our variable.
    - Syntax: `$$foo = "something";`
    - Example: 
        `<?php`<br/>
        `$foo = "bar"; // foo has value "bar"`<br/>
        `$$foo = "data"; // bar has value "data"`<br/>
        `echo "\$foo:\t"; `<br/>
        `echo $foo; //prints bar`<br/>
        `echo "\n";` <br/>
        `echo "\${\$foo}:\t"; `<br/>
        `echo ${$foo}; //prints data`<br/>
        `echo "\n";`<br/>
        `echo "\$\$foo:\t"; `<br/>
        `echo $$foo; //prints data`<br/>
        `echo "\n";`<br/>
        `echo "\$bar:\t"; `<br/>
        `echo $bar; //prints data`<br/>
        `echo "\n";`<br/>
        `?>`<br/><br/>

- Using `{}` is only mandatory when the name of the variable is itself an expression, like this:
    - Example:
        `<?php`<br/>
        `${$variableNamePart1 . $variableNamePart2} = $value;`<br/>
        `?>`<br/><br/><br/>


## Constants
- Variables that cannot be modified during the execution of the script. They are created using the `const` statement or the `define` function.
- You can write constants in camel-case or all uppercase letters.
    - Example: <br/>
    `<?php`<br/>
        `const PI = 3.14; // float`<br/>
        `define("EARTH_IS_FLAT", false); // boolean`<br/>
        `const UNKNOWN = null; // null`<br/>
        `define("APP_ENV", "dev"); // string`<br/>
        `const MAX_SESSION_TIME = 60 * 60; // integer, using (scalar) expressions is ok`<br/>
        `const APP_LANGUAGES = ["de", "en"]; // arrays`<br/>
        `define("BETTER_APP_LANGUAGES", ["lu", "de"]); // arrays`<br/>
    `?>`<br/><br/>

- If you have already defined one constant, you can define another one based on it:
    - Example:
    `<?php`<br/>
        `const TAU = PI * 2;`<br/>
        `define("EARTH_IS_ROUND", !EARTH_IS_FLAT);`<br/>
        `define("MORE_UNKNOWN", UNKNOWN);`<br/>
        `define("APP_ENV_UPPERCASE", strtoupper(APP_ENV)); // string manipulation is ok too`<br/>
        `define("MAX_SESSION_TIME_IN_MINUTES", MAX_SESSION_TIME / 60);`<br/>
        `const APP_FUTURE_LANGUAGES = [-1 => "es"] + APP_LANGUAGES; // array manipulations`<br/>
        `define("APP_BETTER_FUTURE_LANGUAGES", array_merge(["fr"],BETTER_APP_LANGUAGES));`<br/>
    `?>`<br/><br/>

### Checking if constant is defined
- The following code shows how you can use the `defined` function to check if the constants GOOD and AWESOME exist or not. 
    - Example: <br/>
        `<?php`<br/>
            `define("GOOD", false);`<br/>
            `if (defined("GOOD")) {`<br/>
            `echo "GOOD is defined.\n" ; // prints "GOOD is defined"`<br/>
            `if (GOOD)`<br/>
                `echo "GOOD is true." ; // does not print anything, since GOOD is false`<br/>
            `else `<br/>
                `echo "GOOD is false.";`<br/>
            `}`<br/>
            `if (!defined("AWESOME")) {`<br/>
            `define("AWESOME", true); // awesome was not defined. Now we have defined it`<br/>
            `}`<br/>
        `?>`<br/><br/>

### Getting all the defined Constants
- To get all defined constants, including those created by PHP, use the PHP function `get_defined_constants`. The following code snippet shows how this is done:
    - Example: <br/>
        `<?php`<br/>
            `$constants = get_defined_constants();`<br/>
            `var_dump($constants); // prints a very large list`<br/>
        `?>`<br/><br/>
- To get only those constants that were defined by your app call the function at the beginning and at the end of your script (normally after the bootstrap process). Take a look at the following code snippet:
    - Example:<br/>
        `<?php`<br/>
            `$constants = get_defined_constants();`<br/>
            `define("HELLO", "hello");`<br/>
            `define("WORLD", "world");`<br/>
            `$new_constants = get_defined_constants();`<br/>
            `$myconstants = array_diff_assoc($new_constants, $constants); //compares array keys and values, and returns the differences.`<br/>
            `var_export($myconstants); //return the structured value of $myconstants `<br/>
        `?> `<br/><br/>

### Using Constants
- To use a constant just simply use its name
    - Example: <br/>
        `<?php`<br/>
            `//definition`<br/>
            `define("EARTH_IS_FLAT", false); // boolean`<br/>
            `define("APP_ENV_UPPERCASE", "DEV"); // string`<br/>
            `//usage`<br/>
            `if (EARTH_IS_FLAT)`<br/>
            `echo "Earth is flat.\n";`<br/>
            `else`<br/>
            `echo "Earth is round.\n";`<br/>
            `echo APP_ENV_UPPERCASE;`<br/>
        `?>`<br/><br/>
- If you don’t know the name of the constant in advance, use the constant function:
    - Example: <br/>
        `<?php`<br/>
            `//definition`<br/>
            `define("EARTH_IS_FLAT", false); // boolean`<br/>
            `define("APP_ENV_UPPERCASE", "DEV"); // string`<br/>
            `$const1 = "EARTH_IS_FLAT";`<br/>
            `$const2 = "APP_ENV_UPPERCASE";`<br/>
            `if (constant($const1)) `<br/>
                `echo "Earth is flat.\n";`<br/>
            `else`<br/>
                `echo "Earth is round.\n";`<br/>
                `echo constant($const2);`<br/>
        `?>`