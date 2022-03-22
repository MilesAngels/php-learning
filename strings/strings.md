# Strings
## String Interpolation
- The term interpolation refers to the insertion of a variable within a string. Interpolation works in double-quoted strings and the heredoc syntax only.
    - Example: <br/>
`<?php`<br/>
&emsp;`$name = 'Joel';`<br/>
&emsp;`echo "Hello $name, Nice to see you."; // $name will be replaced with "Joel"`<br/>
`?>`<br/><br/>

## Curly Syntax (or complex syntax)
-  It requires that you wrap your variable within curly braces `{}`.
- This can be useful when embedding variables within the text and helps prevent possible ambiguity between text and variables.
- Example: <br/>
`<?php`<br/>
&emsp;`$name = 'Joel';`<br/>
&emsp;`// Example using the curly brace syntax for the variable $name`<br/>
&emsp;`echo "We need more {$name}s to help us!\n";`<br/>
`?>`<br/>