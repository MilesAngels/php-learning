# Introduction To Classes
## What are Classes?
- Classes are the blueprints of objects. 
- A class contains both data and functions to form a package.
- A class is a user-defined data type, which includes local methods and local variables.

## What are Objects?
- An object is an individual instance of the data structure defined by a class.
- We define a class once and then make many objects.

### Inside an Object
- Objects are divided into two parts
    - property
    - method

#### Property 
- The variables inside the class or object

#### Method
- Refer to functions inside the class or object

## The what and the why?
- We use classes and objects to make our code efficient and group similar tasks to make the code less repetitive.
- A class is used to define the actions and data structure is used to build objects.

# Defining Classes
## Syntax for Defining Classes
- To define a class, we need to use the keyword `class` followed by the name you want to give to your new class.
    - Syntax:<br/>
> `class className {`<br/>
> `//properties and methods`<br/>
> `}`<br/>
<br/>

- Example: <br/>
`<?php`<br/>
&emsp;`class Shape{`<br/>
&emsp;&emsp;`public $sides = 0; // first property`<br/>
&emsp;&emsp;`public $name= " "; // second property`<br/> 
&emsp;&emsp;`public function description(){ //first method`<br/>
&emsp;&emsp;&emsp;`echo "A $this->name with $this->sides sides.";`<br/>
&emsp;&emsp;`}`<br/>
&emsp;`}`<br/>
`?>`<br/><br/>