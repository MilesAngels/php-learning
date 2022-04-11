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

- php without catch<br>
`<?php`<br>
&emsp;`function division($a, $b){`<br>
&emsp;&emsp;`    if($b ==0){`<br>
&emsp;&emsp;&emsp;`        throw new Exception('Divisor is zero'); // Throw exception if divisor is zero`<br>
&emsp;&emsp;`    }`<br>
&emsp;&emsp;` else{`<br>
&emsp;&emsp;&emsp;`        $c = $a/$b;`<br>
&emsp;&emsp;&emsp;`        echo "$a / $b = $c";`<br>
&emsp;&emsp;`    }`<br>
&emsp;`}`<br>
` `<br>
&emsp;`try{`<br>
&emsp;&emsp;`    division(10, 2);`<br>
&emsp;&emsp;`    division(15, 0);`<br>
&emsp;&emsp;`    division(30, -4);`<br>
&emsp;&emsp;`   `<br>
&emsp;&emsp;`    `<br>
&emsp;&emsp;`    echo 'All calculations done!';// If an exception is thrown, this line will not execute`<br>
&emsp;`  }`<br>
` `<br>
`// write your catch statement here`<br>
`   `<br>
&emsp;`echo "\n"."Hello World!"; // Continue execution`<br>
`?>`<br><br>

- php with catch <br>
`<?php`<br>
&emsp;`function division($a, $b){`<br>
&emsp;`    `<br>
&emsp;&emsp;`    if($b ==0){`<br>
&emsp;&emsp;&emsp;`        throw new Exception('Divisor is zero'); // Throw exception if divisor is zero`<br>
&emsp;&emsp;`    }`<br>
&emsp;&emsp;` else{`<br>
&emsp;&emsp;`        `<br>
&emsp;&emsp;&emsp;`        $c = $a/$b;`<br>
&emsp;&emsp;&emsp;`        echo "$a / $b = $c";`<br>
&emsp;&emsp;`    }`<br>
&emsp;`}`<br>
&emsp;`   `<br>
&emsp;`try{`<br>
&emsp;&emsp;`    division(10, 2);`<br>
&emsp;&emsp;`    division(15, 0);`<br>
&emsp;&emsp;`    division(30, -4);`<br>
&emsp;&emsp;`   `<br>
&emsp;&emsp;`    `<br>
&emsp;&emsp;`    echo 'All calculations done!';// If an exception is thrown, this line will not execute`<br>
&emsp;`}`<br>
&emsp;` `<br>
&emsp;`catch(Exception $e){   ` <br> 
&emsp;&emsp;` `   <br> 
&emsp;&emsp;`    echo "\n". "Caught <br>exception: " . $e->getMessage(); //Exception handling ` <br>
&emsp;`}`<br>
&emsp;`   `<br>
&emsp;`// write your catch statement here`<br>
&emsp;`   `<br>
&emsp;`echo "\n"."Hello World!"; // Continue execution`<br>
`?>`

## Custom Exceptions
### Defining Custome Exceptions
- The class must be an extension of the built-in exception class since it is the base class.
- The custom class inherits all the objects, properties, and methods of the base class.<br>

`<?php`<br>
&emsp;`  class DecelerationException extends Exception{} //DecelerationException inherits Exception`<br>
&emsp;`  class TimeException extends Exception{} //TimeException inherits Exception`<br>
&emsp;`   `<br>
&emsp;`function acceleration($finalSpeed,$initialSpeed,$time){`<br>
&emsp;&emsp;`   `<br>
&emsp;&emsp;`  if($time <= 0){`<br>
&emsp;&emsp;`    throw new TimeException('Time cannot be negative or zero.'); // Throw exception if time is negative or zero`<br>
&emsp;&emsp;`  } `<br>
&emsp;&emsp;`  if($initialSpeed > $finalSpeed){`<br>
&emsp;&emsp;`    throw new DecelerationException('It is deceleration.'); // Throw exception if initial speed is greater than final speed`<br>
&emsp;&emsp;`  } `<br>
&emsp;&emsp;`  else{`<br>
&emsp;&emsp;&emsp;`    $a = ($finalSpeed-$initialSpeed)/$time;`<br>
&emsp;&emsp;&emsp;`    echo "($finalSpeed-$initialSpeed)/$time = $a";`<br>
&emsp;&emsp;`  }`<br>
&emsp;`}`<br>
&emsp;`try{`<br>
&emsp;&emsp;`  acceleration(20,10, 2);`<br>
&emsp;&emsp;`  acceleration(30,10, -4); //code will stop execution at this point and start finding the catch block`<br>
&emsp;&emsp;`  acceleration(15,20, 5); //$initialSpeed>$finalSpeed`<br>
&emsp;&emsp;`   `<br>
&emsp;&emsp;`  echo 'All calculations done!';// If an exception is thrown, this line will not execute`<br>
&emsp;`} `<br>
&emsp;`   `<br>
&emsp;`catch(DecelerationException $e){`<br>
&emsp;`   `<br>
&emsp;`  echo "\n". "Caught deceleration exception: " . $e->getMessage(); //Exception handling  `<br>
&emsp;`}`<br>
&emsp;`catch(TimeException $e){`<br>
&emsp;`   `<br>
&emsp;&emsp;`  echo "\n". "Caught time exception: " . $e->getMessage(); //Exception handling  `<br>
&emsp;`}`<br>
&emsp;`   `<br>
&emsp;`echo "\n"."Hello World!"; // Continue execution`<br>
`?>`<br><br>
