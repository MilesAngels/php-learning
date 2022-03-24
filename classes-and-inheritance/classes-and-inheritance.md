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

## Creating The Object
- You can create an instance of an object after defining the class.
- For the previous example, we can create an object called Square, Circle, Triangle, etc.
    - Here is how you would create a new object:<br/>
> `$objectName = new ClassName;` 
<br/>

- We use the keyword `new` to create a new instance of a class.
    - Example: <br/>
> `$triangle = new Shape;`
<br/>

## Accessing Class Member Variables
- we can access class members by using the arrow function to call them outside of the class.
    - Example: <br/>
`<?php`<br/>
&emsp;`class Shape`<br/>
&emsp;`{`<br/>
&emsp;&emsp;`public $side = 0;`<br/>
&emsp;&emsp;`public $name = " ";`<br/>
&emsp;&emsp;`public function description()`<br/>
&emsp;&emsp;`{`<br/>
&emsp;&emsp;&emsp;`echo "A $this->name with $this->sides sides.";`<br/>
&emsp;&emsp;`}`<br/>
&emsp;`}`<br/>
&emsp;`$myShape1 = new Shape; //creating an object called myShape1`<br/>
&emsp;`$myShape1->sides = 3; //setting the "sides" property to 3`<br/>
&emsp;`$myShape1->name = "triangle"; //setting the "name" property to triangle`<br/>
&emsp;`$myShape1->description(); //"A triangle with 3 sides"`<br/>
&emsp;`echo "\n";`<br/>
&emsp;`$myShape1->sides = 4; //setting the "sides" property to 4`<br/>
&emsp;`$myShape1->name = "square"; //setting the "name" property to square`<br/>
&emsp;`$myShape1->description(); //"A square with 4 sides"`<br/>
&emsp;`echo "\n";`<br/>
&emsp;`$myShape1->sides = 6; //setting the "sides" property to 6`<br/>
&emsp;`$myShape1->name = "hexagon"; //setting the "name" property to hexagon`<br/>
&emsp;`$myShape1->description(); //"A hexagon with 6 sides"`<br/>
`?>`<br/><br/>