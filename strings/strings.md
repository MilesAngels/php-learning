# Strings
## String Interpolation
- The term interpolation refers to the insertion of a variable within a string. Interpolation works in double-quoted strings and the heredoc syntax only.
    - Example: <br/>
`<?php`<br/>
&emsp;`$name = 'Joel';`<br/>
&emsp;`echo "Hello $name, Nice to see you."; // $name will be replaced with "Joel"`<br/>
`?>`<br/><br/>

### Curly Syntax (or complex syntax)
-  It requires that you wrap your variable within curly braces `{}`.
- This can be useful when embedding variables within the text and helps prevent possible ambiguity between text and variables.
- Example: <br/>
`<?php`<br/>
&emsp;`$name = 'Joel';`<br/>
&emsp;`// Example using the curly brace syntax for the variable $name`<br/>
&emsp;`echo "We need more {$name}s to help us!\n";`<br/>
`?>`<br/><br/>
> You will get an error if you add an s to a variable that isn't in curly syntax
> Variable name: $name
> This will give you an error: $names
> This is completely okay: {$name}s
<br/>

> ***Make sure that you do not forget the `$` when trying to interpolate variables with a string.***

## String Operators
- There are only two string operators:
    - Concatenation (`.`)
    - Concatenation Assignment(`.=`)

### Concatenation
- The most important operation in strings is concatenation. It means joining one string to another.
- Example: <br/>
`<?php`<br/>
&emsp;`$a = "water";`<br/>
&emsp;`$b = "bottle";`<br/>
&emsp;`$c = $a . $b; // $c => "ab"`<br/>
&emsp;`echo $c;`<br/>
`?>`<br/><br/>

### Concatenation Assignment
- Concatenation assignment is a slight variation of concatenation where you concatenate (add) one string at the end of another without the need for a third destination string.
- Example: <br/>
`<?php`<br/>
&emsp;`$a = "a";`<br/>
&emsp;`$a .= "b"; // $a => "ab"`<br/>
&emsp;`echo $a;`<br/>
`?>`<br/><br/>

## Built-in Functions
### Extracting or Replacing Substrings
- Single characters can be extracted using array (square brace) syntax as well as curly brace syntax. This will only return a single character.
- If we need more than one character, we have to use the in-built `substr` function.
- Example: <br/>
`<?php`<br/>
&emsp;`$foo = 'Hello world';`<br/>
&emsp;`echo $foo[6]; // returns 'w'//extracting a single character`<br/>
&emsp;`echo "\n";`<br/>
&emsp;`echo $foo{6}; // also returns 'w'`<br/>
&emsp;`echo "\n";`<br/>
&emsp;`echo substr($foo, 6, 1); // also returns 'w'`<br/>
&emsp;`echo "\n";`<br/>
&emsp;`echo substr($foo, 6, 2); // returns 'wo'//extracting multiple characters`<br/>
`?>`<br/><br/>

### Finding Position of a Substring
- In PHP you can use the `strpos` method to get the position/occurrence of a substring in another string.
- If the substring does not exist, the `strpos` returns `false`.
- Example: <br/>
`<?php`<br/>
&emsp;`echo "The occurence of hay is at position: ".strpos("haystack", "hay")."\n"; // int(0)`<br/>
&emsp;`echo "The occurence of stack is at position: ".strpos("haystack", "stack")."\n"; // int(3)`<br/>
`?>`<br/><br/>

### Replacing Characters in a String
- Strings can also be changed one character at a time using the same square brace and curly brace syntax.
- Replacing more than one character requires a function, `substr_replace`.
- Example:<br/>
`<?php`<br/>
 &emsp;`$foo = 'hello world';`<br/>
 &emsp;`$foo[6] = 'W'; // capitalizes the 'w' in 'hello world'`<br/>
 &emsp;`echo $foo;`<br/>
 &emsp;`echo "\n";`<br/>
 &emsp;`$foo{0} = 'H'; // capitalizes the 'h' in 'hello world'`<br/>
 &emsp;`echo $foo;`<br/>
 &emsp;`echo "\n";`<br/>
 &emsp;`$bar = substr_replace($foo, '!', 11, 1); // results in $bar = 'Hello World!'`<br/>
 &emsp;`echo $bar;`<br/>
 &emsp;`echo "\n";`<br/>
 &emsp;`$bar = substr_replace($foo, 'Whi', 6, 2); // results in 'Hello Whirld'`<br/>
 &emsp;`// Note that the replacement string need not be the same length as the substring replaced`<br/>
 &emsp;`echo $bar;`<br/>
 &emsp;`echo "\n";`<br/>
`?>`<br/><br/>

> Note: The `substr_replace` function does not change the actual string. It just returns the new string that would???ve been made after doing the replacement under discussion.

- You can do this using the `str_replace()` method which essentially replaces all occurrences of the search text within the target string.
    - Example: <br/>
`<?php`<br/>
&emsp;`$my_str = 'If the facts do not fit the theory, change the facts.';`<br/>
&emsp;`// replaces "facts" with "truth" and displays new string`<br/>
&emsp;`echo str_replace("facts", "truth", $my_str);`<br/>
`?>`<br/><br/>

- You can pass a fourth argument to the `str_replace()` function to know how many times the string replacements were performed, like so:
`<?php`<br/>
&emsp;`$my_str = 'If the facts do not fit the theory, change the facts.';`<br/>
&emsp;`// Perform string replacement`<br/>
&emsp;`str_replace("facts", "truth", $my_str, $count);`<br/>
&emsp;`// Display number of replacements performed`<br/>
&emsp;`echo "The text was replaced $count times.";`<br/>
`?>`<br/><br/>

### Calculating the Length of a String
- The `strlen()` function is used to calculate the number of characters inside a string. It also includes the blank spaces inside the string.
- Example:<br/>
`<?php`<br/>
&emsp;`$my_str = 'Welcome to Educative!';`<br/>
&emsp;`echo strlen($my_str);`<br/>
`?>`<br/><br/>

### Counting the Number of Words in a String
- The `str_word_count()` function counts the number of words in a string.
- Example:<br/>
`<?php`<br/>
&emsp;`$my_str = 'The quick brown fox jumps over the lazy dog.';`<br/>
&emsp;`echo str_word_count($my_str);`<br/>
`?>`<br/><br/>

### Reversing a String
- The `strrev()` function in PHP can be used to reverse a string.
- Example:<br/>
`<?php`<br/>
&emsp;`$my_str = 'You can do anything, but not everything.';`<br/>
&emsp;`// Display reversed string`<br/>
&emsp;`echo strrev($my_str);`<br/>
`?>`<br/><br/>
