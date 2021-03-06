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

> **Output**<br/>
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

- Array that have arrays in every indices.<br/> 
`<?php`<br/>
&emsp;`$comparisonAdjectives = array(`<br/>
&emsp;&emsp;    `array(`<br/>
&emsp;&emsp;&emsp;        `"good",`<br/>
&emsp;&emsp;&emsp;        `"better",`<br/>
&emsp;&emsp;&emsp;        `"best"`<br/>
&emsp;&emsp;    `) ,`<br/>
&emsp;&emsp;    `array(`<br/>
&emsp;&emsp;&emsp;        `"bad",`<br/>
&emsp;&emsp;&emsp;        `"worse",`<br/>
&emsp;&emsp;&emsp;        `"worst"`<br/>
&emsp;&emsp;    `) ,`<br/>
&emsp;&emsp;    `array(`<br/>
&emsp;&emsp;&emsp;        `"tall",`<br/>
&emsp;&emsp;&emsp;        `"taller",`<br/>
&emsp;&emsp;&emsp;        `"tallest"`<br/>
&emsp;&emsp;    `)`<br/>
&emsp;`);`<br/>
&emsp;`print_r($comparisonAdjectives);`<br/>
`?>`<br/><br/> 

> **Output**<br/>
> &emsp;`Array`<br/>
> &emsp;`(`<br/>
> &emsp;&emsp;    `[0] => Array`<br/>
> &emsp;&emsp;        `(`<br/>
> &emsp;&emsp;&emsp;            `[0] => good`<br/>
> &emsp;&emsp;&emsp;            `[1] => better`<br/>
> &emsp;&emsp;&emsp;           `[2] => best`<br/>
> &emsp;&emsp;        `)`<br/>
> &emsp;&emsp;    `[1] => Array`<br/>
> &emsp;&emsp;       `(`<br/>
> &emsp;&emsp;&emsp;            `[0] => bad`<br/>
> &emsp;&emsp;&emsp;            `[1] => worse`<br/>
> &emsp;&emsp;&emsp;            `[2] => worst`<br/>
> &emsp;&emsp;        `)`<br/>
> &emsp;&emsp;    `[2] => Array`<br/>
> &emsp;&emsp;        `(`<br/>
> &emsp;&emsp;&emsp;            `[0] => tall`<br/>
> &emsp;&emsp;&emsp;            `[1] => taller`<br/>
> &emsp;&emsp;&emsp;            `[2] => tallest`<br/>
> &emsp;&emsp;        `)`<br/>
> &emsp;`)`<br/><br/>

- An equivalent method of declaring the array above is the following:<br/>
`<?php`<br/>
&emsp;`$comparisonAdjectives[0][0] = "good";`<br/>
&emsp;`$comparisonAdjectives[0][1] = "better";`<br/>
&emsp;`$comparisonAdjectives[0][2] = "best";`<br/>
&emsp;`$comparisonAdjectives[1][0] = "bad";`<br/>
&emsp;`$comparisonAdjectives[1][1] = "worse";`<br/>
&emsp;`$comparisonAdjectives[1][2] = "worst";`<br/>
&emsp;`$comparisonAdjectives[2][0] = "tall";`<br/>
&emsp;`$comparisonAdjectives[2][1] = "taller";`<br/>
&emsp;`$comparisonAdjectives[2][2] = "tallest";`<br/>
&emsp;`print_r($comparisonAdjectives);`<br/>
`?>` <br/><br/>

## Accessing values in Multidimensional Arrays
- We can access a particular value from a multidimensional array using keys of subsequent arrays.
- using the example array `$comparisionAdjectives`, we can specify or access a specific value
    - `echo $comparisonAdjective[1][2];` this will output `"worst"` since it is in index 1 and in index 2 within that array.

## Indexed Array of Associative Arrays
- Indexed array containing associative arrays<br/>
`<?php`<br/>
&emsp;`// Define a multidimensional array`<br/>
&emsp;`$economy = array(`<br/>
&emsp;&emsp;    `array(`<br/>
&emsp;&emsp;&emsp;        `"country" => "Germany",`<br/>
&emsp;&emsp;&emsp;        `"currency" => "Euro",`<br/>
&emsp;&emsp;    `),`<br/>
&emsp;&emsp;    `array(`<br/>
&emsp;&emsp;&emsp;        `"country" => "Switzerland",`<br/>
&emsp;&emsp;&emsp;        `"currency" => "Swiss Franc",`<br/>
&emsp;&emsp;    `),`<br/>
&emsp;&emsp;    `array(`<br/>
&emsp;&emsp;&emsp;        `"country" => "England",`<br/>
&emsp;&emsp;&emsp;        `"currency" => "Pound",`<br/>
&emsp;&emsp;   `)`<br/>
&emsp;`);`<br/>
&emsp;`echo "Currency of Germany is: " . $economy[0]["currency"]; // Access array at [0] index`<br/>
`?>`<br/><br/>

***Challenge 2***

# Adding Elements in an Array
## Adding Elements at the Start
- You can add an element at the beginning of an array without modifying any of the current elements within the array by using `array_unshift()`
    - It prepends passed elements at the front of an array. 
### Using array_unshift()
- It has 2 or more parameters: first is the name of the array, the other parameters are the elements that need to be added to an array.
    - Example: <br/>
`<?php`<br/>
&emsp;`$myArray = array(1, 2, 3);`<br/>
&emsp;`array_unshift($myArray, 4,5);`<br/>
&emsp;`print_r($myArray)`<br/>
`?>`<br/><br/>

## Adding Elements at the End
- You can add an element at the end of an array without modifying any of the current elements within the array by using `array_push()`
    - It pushed one or more element at the end of an array. 
### Using array_push()
- It has 2 or more parameters: the first parameter is the name of an array, and the other parameters are the elements to be added at the end of that array.
    - Example: <br/>
`<?php`<br/>
&emsp;`$array = [1,2,3];`<br/>
&emsp;`print_r($array);`<br/>
&emsp;`array_push($array, 5, 6); // Pushing 5 and 6 at the end of $array`<br/>
&emsp;`print_r($array); `<br/>
`?>` <br/><br/>  

# Adding and Replacing Values at Random Position in an Array
- To add or replace values at any position in an array, access the array position and assign a value.

    > `$arrayName[key]=value;`<br/>
    - If an old key is used to assign a new value, the old value will be replaced.
    - If a new key is used to assign a value, a new key will be created in the array.
<br/>

- Example: <br/>
`<?php`<br/>
&emsp;`$arr=array(1,3,5,7,9);`<br/>
&emsp;`$arr[23]=71; // adding a new key and its assocaited value`<br/>
&emsp;`print_r($arr);`<br/>
&emsp;`$arr[2]=22; // replacing an old value at 2nd index`<br/>
&emsp;`print_r($arr);`<br/>
`?>`<br/><br/>

# Removing Elements from Arrays
## Removing Elements from Indexed Arrays
- The PHP built-in function `unset()` is used to remove an element from an array.
    - By specifying an array element as an input parameter for `unset()` will remove that element from an indexed array and its key.
    - Example: <br/>
`<?php`<br/>
&emsp;`$fruit = array("bananas", "apples", "peaches");`<br/>
&emsp;`unset($fruit[1]);`<br/>
&emsp;`print_r($fruit);`<br/>
`?>` <br/><br/>   

> `unset()` does not change the keys (indexes in this case) of the remaining elements.

<br/>

## Removing Elements from Associative Arrays
- We can remove an element in an associative array by specifying the element that we want to remove using `unset()`
    - Example: <br/>
`<?php`<br/>
&emsp;`$fruit = array('first'=>'banana', 'second'=>'apple', 'third'=>'peaches');`<br/>
&emsp;`unset($fruit['third']);`<br/>
&emsp;`print_r($fruit);`<br/>
`?>`<br/><br/>

# Sorting Arrays
## Sorting Indexed Arrays
### By Value
- We can sort arrays by utilizing the built-in function `sort()` in ascending order.
- The associated keys will not be preserved during this.
    - Example:<br/>
`<?php`<br/> 
&emsp;`$fruits = ['Rasberry', 'Orange', 'Apricot','Banana', 'Apple','Olive' ]; //defining and array`<br/>
&emsp;`sort($fruits); //applying the sort function`<br/>
&emsp;`print_r($fruits); //printing the sorted array`<br/>
`?>`<br/><br/>   

## Sorting Associative Arrays
### By Value
- We can sort associative arrays by value using the built-in function `asort()`. This will sort the array in *ascending order*.
- `asort()` sorts the a associative array on values.
- Keys with each value will be preserved.
    - Example:<br/>
`<?php`<br/> 
&emsp;`$fruits = [1=>'Rasberry',2=> 'Orange',3=> 'Apricot',4=>'Banana', 5=>'Apple',6=>'Olive' ]; //defining and array`<br/>
&emsp;`asort($fruits); //applying the sort function`<br/>
&emsp;`print_r($fruits); //printing the sorted array`<br/>
`?>`  <br/><br/>   

- We can sort associative arrays by value another way. We can use the built-in function `arsort()` to sort associative arrays in descending order.
    - Example: <br/>
`<?php`<br/> 
&emsp;`$fruits = [1=>'Rasberry',2=> 'Orange',3=> 'Apricot',4=>'Banana', 5=>'Apple',6=>'Olive' ]; //defining and array`<br/>
&emsp;`arsort($fruits); //applying the sort function`<br/>
&emsp;`print_r($fruits); //printing the sorted array`<br/>
`?>`<br/><br/> 

## By Key
- We can sort associative arrays by key. We will need to use `ksort()` to do so and this will sort the array in ascending order.
- The associated values are preserved during this sort.
    - Example: <br/>
`<?php`<br/>
&emsp;`$fruits = ['f'=>'Rasberry','d'=>'Orange','a'=> 'Apricot','c'=>'Banana', 'b'=>'Apple','e'=>'Olive' ]; //defining and array`<br/>
&emsp;`ksort($fruits); //applying the sort function`<br/>
&emsp;`print_r($fruits); //printing the sorted array`<br/>
`?>`<br/><br/>

- We can sort associative arrays by key in descending order by using the `krsort()` which is a buil-in funtion.
- The associated values are preserved during this sort.
    - Example: <br/>
`<?php`<br/> 
&emsp;`$fruits = ['d'=>'Rasberry','b'=>'Orange','a'=> 'Apricot','e'=>'Banana', 'f'=>'Apple','c'=>'Olive' ]; //defining and array`<br/>
&emsp;`krsort($fruits); //applying the sort function`<br/>
&emsp;`print_r($fruits); //printing the sorted array`<br/>
`?>`<br/><br/> 

# Merging Arrays
## The array_merge() function
- The easiest way to merge 2 or more arrays is to use the built-in function `array_merge()`.
- It can take as many input parameters as you'd want and it will return the merged array.

### Indexed Array
- For indexed arrays, `array_merge()` will merge multiple arrays without overwriting the value of one of the arrays but will append them instead. 
- All the new appended elements will be renumbered.
    - Example: <br/>
`<?php`<br/>
&emsp;`$a1 = array("red","green");`<br/>
&emsp;`print_r($a1);`<br/>
&emsp;`$a2 = array("blue","yellow");`<br/>
&emsp;`print_r($a2);`<br/>
&emsp;`$a3=array("black");`<br/>
&emsp;`print_r($a3);`<br/>
&emsp;`print_r(array_merge($a1,$a2,$a3));`<br/>
`?>`<br/><br/>

### Associative Array
- For associative arrays, `array_merge()` will merge multiple arrays together.
    - If the arrays have the same string keys then, the later value for that key will overwrite the previous one.
    - Example: <br/>
`<?php`<br/>
&emsp;`$a1=array("a"=>"red","b"=>"green");`<br/>
&emsp;`$a2=array("c"=>"blue","b"=>"yellow");`<br/>
&emsp;`$a3=array("e"=>3);`<br/>
&emsp;`print_r(array_merge($a1,$a2,$a3));`<br/><br/>
`?>`<br/><br/>