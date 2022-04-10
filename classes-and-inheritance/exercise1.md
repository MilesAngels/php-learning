# Calculating Area
## Problem Statement
- Let’s start with a very basic example.
- Write a class called Triangle having two public variables for length and height and one member function called area which will return the area of the right angle triangle. You can calculate the area of a triangle using
- Area = 1/2(length)(height)

## Input 
- Two variables (integer or float) as the dimensions of the triangle
## Output
- area of that triangle

>`<?php`<br>
>`//define your class here`<br>
>`// name your class Triangle`<br>
>`//name your function area`<br>
>`class Triangle {`<br>
>`  public $length = 0;`<br>
>`  public $height = 0;`<br>
>`  public function area() {`<br>
>`    return (($this->length * $this->height)/2);`<br>
>`  }`<br>
>`}`<br>
>`  `<br>
>` `<br>
>`//This is a test function. Do not change it.`<br>  
>`function test($length, $height) {`<br>
>` `<br>
>`  $answer=0;`<br>
>`  $obj = new Triangle;`<br>
>`  $obj->length= $length;`<br>
>`  $obj->height= $height;`<br>
>`  echo "Area: ".$obj->area();`<br>
>`  $answer = $obj->area();`<br>
>` `<br>
>`  return $answer;`<br>
>`}`<br>
>`?>`<br><br>