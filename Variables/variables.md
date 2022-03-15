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
                `?>`<br/><br/><br/>