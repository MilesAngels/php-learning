# PHP Exception
## What is an exception?
- An exception is an unexpected program result that can be handled by the program itself.
## What happens when an exception is trigerred?
- When an exception is trigerred, the current code state is saved.
- The code will execute a predefined custom exception handler function.
## Exception handling in PHP
- specialized keywords for exception handling
    - try
    - throw
    - catch
    - finally

## Exception Class
- PHP has a built-in Exception class with various methods and properties.
### Components
- `try`: It is a block of code which exception may arise
- `catch`: It is a block of code that will be executed when a particular exception is thrown
- `throw`: It is used to throw an exception. It is also used to list the exceptions that a function throws, but doesn't handle itself.
- `finally`: This is the block of code that executes at the end once the exception is thrown and/or handled.
<br><br>

`<?php`<br>
&emsp;`function distance($speed, $time){`<br>
&emsp;`    `<br>
&emsp;&emsp;`    if($time <= 0){`<br>
&emsp;&emsp;`        throw new Exception('Time cannot be zero or negative.'); // Throw exception if time is negative`<br>
&emsp;&emsp;`    }`<br>
&emsp;&emsp;` else{`<br>
&emsp;&emsp;&emsp;`        `<br>
&emsp;&emsp;&emsp;`        $d = $speed*$time;`<br>
&emsp;&emsp;&emsp;`        echo "$speed * $time = $d";`<br>
&emsp;&emsp;`    }`<br>
&emsp;`}`<br>
&emsp;` `<br>
&emsp;`try{`<br>
&emsp;&emsp;`    distance(10,2);`<br>
&emsp;&emsp;`    distance(30,-4); //code will stop execution at this point (due to negative time) and start finding the catch block`<br>
&emsp;&emsp;`    distance(15,3);`<br>
&emsp;&emsp;`    `<br>
&emsp;&emsp;`    echo 'All calculations done!'; // If an exception is thrown, this line will not execute`<br>
&emsp;`  } `<br>
&emsp;` `<br>
&emsp;`// catch block is executed when an exception is thrown in the try block`<br>
&emsp;`// an object $e of Exception class is created`<br>
&emsp;`catch(Exception $e){    ` <br>
&emsp;&emsp;`    `<br>
&emsp;&emsp;`    echo "\n". "Caught exception: " . $e->getMessage(); //Exception handling ` <br>
&emsp;`}`<br>
&emsp;` `<br>
&emsp;`echo "\n"."Hello World!"; // Continue execution`<br>
`?>`<br><br>

### Methods
- PHP Exception class provides these methods
    - getCode()
    - getFile()
    - getLine()
    - getTraceAsString()
<br>

|php without catch|php with catch|
|-----------------|--------------|
|<?php
|function division($a, $b){
    if($b ==0){
        throw new Exception('Divisor is zero'); // Throw exception if divisor is zero
    } else{
        
        $c = $a/$b;
        echo "$a / $b = $c";
    }
}
 
try{
    division(10, 2);
    division(15, 0);
    division(30, -4);
   
    
    echo 'All calculations done!';// If an exception is thrown, this line will not execute
  }

// write your catch statement here

echo "\n"."Hello World!"; // Continue execution
?>||