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

***Challenge 1***
<br/>

# Multidimensional Arrays
- These arrays contain items that can be a single value or an array itself.
- No limits to the dimensions of a multidemensional array. 
- Array or arrays

## Declaring Multidimensional Arrays
- 2D array declaration:<br/>
    > $arrayName = array(array(), array()....)

- Arrays are resized dynamically and any attempt to write anything to a non-existent element creates it and creates an entire array if needed. 
    - Example: <br/>
`<?php`<br/>
&emsp;`$check=array("elephant", array("honey", "sad", 5));`<br/> 
&emsp;`print_r($check);`<br/>
`?>`<br/>

> **Output**
> `Array`<br/>
> `(`<br/>
> &emsp;`[0] => elephant`<br/>
> &emsp;`[1] => Array`<br/>
> &emsp;&emsp;`(`<br/>
> &emsp;&emsp;&emsp;`[0] => honey`<br/>
> &emsp;&emsp;&emsp;`[1] => sad`<br/>
> &emsp;&emsp;&emsp;`[2] => 5`<br/>
> &emsp;&emsp;`)`<br/>
> `)`<br/>