# SYNTAX
1. using echo to print out statements<br/>
`<?php
    echo "Hello, World!\n";
?>`<br/>
**output will be Hello, World!**<br/>

2. alternatively, you can use print<br/>
`<?php
    print "Hello, World!\n";
?>`<br/>
**output will be Hello, World!**<br/>

3.  PHP C-style print-f <br/>
`<?php
    printf("%\n", "Hello World!");
?>`<br/><br/><br/>


## PHP Opening Tag<br/>
- A PHP script can be written anywhere in the document, and it signifies the start of the PHP code 
`<?php`

1. echo - a built-in function in PHP that is used to display one or more strings
    - The echo function is faster than the print() function.
    - `echo "Hello, World!;"`
    - keyword string semi-colon is the pattern
    - **NOTE: You can use parenheses with the echo function; not necessary**<br/><br/>

## PHP Closing Tag<br/>
- The PHP closing tag marks the end of the PHP code. It is written as `?>`
- **NOTE: All cod ein PHP is written between the opening tag and closing tag. However, the closing tag is optional when we are writing a code block.**<br/><br/>


## Semicolons
- Statements in PHP must be terminated with a semicolon<br/><br/><br/>

# QUIZ
1. It is not required to use parentheses with the echo function. **TRUE**

2. `;?>` is the starting symbol for any PHP program. **FALSE**

3. Which of the following changes would prevent the error from occuring <br/>
`<?php
echo "My name is Jerry"`<br/>
**The end symbol `?>` is missing**

4. You can also use `print` function instead of `echo` function in PHP. **TRUE**


# Challenge: Displaying Output