# Arrays and their Operators
- An array is like a list of values
- Index always starts at 0

## Outputting a Structured View of Arrays
- To print an array, we can use `print_r($arrayName)`
- This will print an array with their keys and their associated values. (NEAT!)
- Example:<br/>
`<?php`<br/>
&emsp;`$fruits = array("Type"=>"Citrus",1=>"Orange",2=>"Grapefruit",3=>"Lemon");//initializing associative array`<br/>
&emsp;`print_r($fruits);`<br/>
`?>`<br/><br/>

- To print a very detailed array, we can use `var_dump()`
    - This will print out keys, their associated values' data type (and length in parenthesis) and the value itself. 
    - Example: <br/>
`<?php`<br/>
&emsp;`$fruits = array("Type"=>"Citrus",1=>"Orange",2=>"Grapefruit",3=>"Lemon");//initializing associative array`<br/>
&emsp;`var_dump($fruits);`<br/>
`?>`<br/><br/>

> `echo` won't be great for trying to output an array.
<br/>

## Length of an Array
- The total number of elements in an array is called the length of an array.
- This length is dynamic which means that we may add or remove items from the array.
- We can check for the length of an array by using `count($arrayName)`
- Example: <br/>
`<?php`<br/>
&emsp;`$fruits = array("Type"=>"Citrus",1=>"Orange",2=>"Grapefruit",3=>"Lemon");//initializing associative array`<br/>
&emsp;`echo "Length of \$fruits is ".count($fruits);`<br/>
`?>`<br/><br/>