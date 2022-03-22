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
`<?php`
&emsp;`$foo = 'Hello world';`
&emsp;`echo $foo[6]; // returns 'w'//extracting a single character`
&emsp;`echo "\n";`
&emsp;`echo $foo{6}; // also returns 'w'`
&emsp;`echo "\n";`
&emsp;`echo substr($foo, 6, 1); // also returns 'w'`
&emsp;`echo "\n";`
&emsp;`echo substr($foo, 6, 2); // returns 'wo'//extracting multiple characters`
`?>`