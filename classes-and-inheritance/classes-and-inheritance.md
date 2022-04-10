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
- we can access class members by using the object operator (`->`) to call them outside of the class.
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

# $this and self
## $this
- `$this` is a pseudo-variable that refers to a member of a class according to an instance of that class.
- It provides a reference to the calling object, that is the object which the method or property belongs to.
### The Object Operator
- The `->` operator is abuilt-in construct that is used with the `$this` keyword to access contained methods and properties.

## self
- The `self` keyword refers to properties and method inside the scope of the class. 
- It provides a reference to the calling object, that is the object which the method or property belongs to.
### The Scope Resolution Operator
- The `::` symbol, known as the scope resolution operator is a buil-in construct that is used to access methods and properties.
<br/>

> #### this versus self
> - Use $this->member for accessing non-static members (methods and properties)
> - Use self::$member for accessing static members (methods and properties)
>       - note: static members are accessible without needing an instantiation of the class and can be accessed statically within an instantiated class object.
<br/>

- Example: <br/>
`<?php`<br/>
&emsp;`class Circle`<br/>
&emsp;`{`<br/>
&emsp;&emsp;`// properties`<br/>
&emsp;&emsp;`public $radius= 0; //declaring public member`<br/>
&emsp;&emsp;`public static $pi=3.14;  //declaring a public static member`<br/>
&emsp;&emsp;`// Method to get the Circumference`<br/>
&emsp;&emsp;`public function getCircumference(){`<br/>
&emsp;&emsp;&emsp;`return (2 * self::$pi * $this->radius );`<br/>
&emsp;&emsp;`}`<br/>
&emsp;&emsp;`// Method to get the area`<br/>
&emsp;&emsp;`public function getArea(){`<br/>
&emsp;&emsp;`return ($this->radius * $this->radius*self::$pi);`<br/>
&emsp;&emsp;`}`<br/>
&emsp;&emsp;`// Method to get the diameter`<br/>
&emsp;&emsp;`public function getDiameter(){`<br/>
&emsp;&emsp;&emsp;`return ($this->radius * 2);`<br/>
&emsp;&emsp;`}`<br/>
&emsp;`}`<br/>
&emsp;`// Create a new Circle class object`<br/>
&emsp;`$obj = new Circle;`<br/>
&emsp;`// Set object properties values`<br/>
&emsp;`$obj->radius = 4;`<br/>
&emsp;`// Read the object properties values again to show the change`<br/>
&emsp;`echo "Radius is ". $obj->radius . "\n";` <br/>
&emsp;`echo "Diamater is ". $obj->getDiameter() . "\n"; `<br/>
&emsp;`// Call the object methods`<br/>
&emsp;`echo "Circumference is ". $obj->getCircumference(),"\n";`<br/>
&emsp;`echo "Area is " .$obj->getArea()."\n";` <br/>
&emsp;`echo "Value of pi is " .$obj::$pi;`<br/>
`?>`<br/><br/>

# Constructors & Destructors
## Constructors
- A constructor is used to initialize member variables when an object is declared.
- It is automatically called at the time when the object of the class is declared.
> **Note**: A constructor is a member function that is usually `public`.
> It **cannot** return a value.

### Constructor Declaration
- Classes can define a special __construct() method, which is executed as part of object creation. 
    - Example: <br/>
`<?php`<br/>
&emsp;`class Shape {`<br/>
&emsp;&emsp;`public $sides = 0;`<br/>
&emsp;&emsp;`public $name = " "; `<br/> 
&emsp;&emsp;`//initializes $name to $Name and $sides to $Sides`<br/>
&emsp;&emsp;`public function __construct($Name, $Sides)` <br/>
&emsp;`}`<br/>
`?>`<br/><br/>

### Constructor Definition
- Example: <br/>
`<?php`<br/>
&emsp;`class Shape`<br/>
&emsp;`{`<br/>
&emsp;&emsp;`public $sides = 0;`<br/>
&emsp;&emsp;`public $name = " ";`<br/>
&emsp;&emsp;`public function __construct($name, $sides)`<br/>
&emsp;&emsp;`{ //defining a constructor`<br/>
&emsp;&emsp;&emsp;`$this->sides = $sides; //initializing $this->sides to $sides`<br/>
&emsp;&emsp;&emsp;`$this->name = $name; //initializing $this->name to $name` <br/>
&emsp;&emsp;`}`<br/>
&emsp;&emsp;`public function description()`<br/>
&emsp;&emsp;`{ //method to display name and sides of a shape`<br/>
&emsp;&emsp;&emsp;`echo "A $this->name with $this->sides sides.";`<br/>
&emsp;&emsp;`}`<br/>
&emsp;`}`<br/>
&emsp;`$myShape = new Shape("hexagon", 6); //making an object and passing values to the constructor`<br/>
&emsp;`$myShape->description(); // A shape with 6 sides`<br/>
`?>`<br/>

### Calling a Constructor
- It is called in object declaration
- It creates a class object
- It calls the constructor to initialize variables

## Destructors
- Destructors are the opposite of constructors, as they define the final behavior of an object and execute when the object is no longer in use.
- an object's destructor, which takes not parameters is called sometime after an object is no longer referenced, but the complexitites of garbage collection make the specific timing of destructors uncertain.
> destructors ar enot called but are invoked automatically

<br/>

- Example: <br/>
`<?php`<br/>
&emsp;`class Shape`<br/>
&emsp;`{`<br/>
&emsp;&emsp;`public $sides = 0;`<br/>
&emsp;&emsp;`public $name = " ";`<br/>
&emsp;&emsp;`public function __construct($name, $sides)`<br/>
&emsp;&emsp;`{ //defining a constructor`<br/>
&emsp;&emsp;&emsp;`$this->sides = $sides; //initializing $this->sides to $sides`<br/>
&emsp;&emsp;&emsp;`$this->name = $name; //initializing $this->name to $name `<br/>
&emsp;&emsp;`}`<br/>
&emsp;&emsp;`public function __destruct()`<br/>
&emsp;&emsp;`{ //destructor for Shape gets called at the end`<br/>
&emsp;&emsp;&emsp;`echo "Destructor Called!\n";`<br/>
&emsp;&emsp;`}`<br/>
&emsp;&emsp;`public function description()`<br/>
&emsp;&emsp;`{ //method to display name and sides of a shape`<br/>
&emsp;&emsp;&emsp;`echo "A $this->name with $this->sides sides.\n";`<br/>
&emsp;&emsp;`}`<br/>
&emsp;`}`<br/>
&emsp;`$myShape = new Shape("hexagon", 6); //making an object and passing values to the constructor`<br/>
&emsp;`$myShape->description(); // A shape with 6 sides`<br/>
`?>`<br/><br/>

# Methods and Property Visibility
- Access modifiers provide access to the varibales of a class. 
- There are three visibility types that you can apply to methods.
    - Public
    - Private
    - Protected
## Public
- Declaring a method or property as `public` allows the method or property to be accessed by:
    - The class that declared it
    - The classes that inherits from the declare class.
    - Any external objects, classes, or code outside the class hierarchy. 
- Example: <br/>
`<?php`<br/>
&emsp;`class Car`<br/>
&emsp;`{`<br/>
&emsp;&emsp;`public $name = " ";`<br/>
&emsp;&emsp;`public function display()`<br/>
&emsp;&emsp;`{`<br/>
&emsp;&emsp;&emsp;`echo "Name: $this->name" . "\n";`<br/>
&emsp;&emsp;`}`<br/>
&emsp;&emsp;`public function __construct($name)`<br/>
&emsp;&emsp;`{`<br/>
&emsp;&emsp;&emsp;`$this->name = $name;`<br/>
&emsp;&emsp;`}`<br/>
&emsp;`}`<br/>
&emsp;`$obj1 = new Car("BMW"); //creating an object of car and setting its name as BMW`<br/>
&emsp;`echo "Name: " . $obj1->name; //accessing the "name" property of obj1 directly outside of class`<br/>
&emsp;`echo "\n";`<br/>
&emsp;`$obj2 = new Car("Mercedes"); //creating an object of car and setting its name as Mercedes`<br/>
&emsp;`echo $obj2->display(); //accessing the "display" method of obj1 directly outside of class`<br/>
`?>`<br/><br/>

## Private
- Declaring a method or property as private allows the method or property to be accessed by:
    - Only the class that declares it
- Only visible and accessible within the class that created it.
- Example: <br/>
`<?php`<br/>
&emsp;`class Car`<br/>
&emsp;`{`<br/>
&emsp;&emsp;`public $name = " ";`<br/>
&emsp;&emsp;`private $plateNumber;`<br/>
&emsp;&emsp;`public function display()`<br/>
&emsp;&emsp;`{`<br/>
&emsp;&emsp;&emsp;`echo "Name: $this->name" . "\n";`<br/>
&emsp;&emsp;`}`<br/>
&emsp;&emsp;`public function setPlateNumber($number)`<br/>
&emsp;&emsp;`{ //sets value of property plateNumber`<br/>
&emsp;&emsp;&emsp;`$this->plateNumber = $number;`<br/>
&emsp;&emsp;`}`<br/>
&emsp;&emsp;`public function getPlateNumber()`<br/>
&emsp;&emsp;`{ //returns the property "plateNumber"`<br/>
&emsp;&emsp;&emsp;`return $this->plateNumber;`<br/>
&emsp;&emsp;`}`<br/>
&emsp;&emsp;`public function __construct($name, $number)`<br/>
&emsp;&emsp;`{`<br/>
&emsp;&emsp;&emsp;`$this->name = $name;`<br/>
&emsp;&emsp;&emsp;`$this->plateNumber = $number;`<br/>
&emsp;&emsp;`}`<br/>
&emsp;`}`<br/>
&emsp;`$obj1 = new Car("BMW", 68775); //making a car object with values of name and platenumber set`<br/>
&emsp;`echo $obj1->display(); //displaying name of car`<br/>
&emsp;`echo "Plate number: " . $obj1->getPlateNumber(); //accessing plateNumber by calling getPlateNumber method`<br/>
&emsp;`echo "\n";`<br/>
&emsp;`$obj1->setPlateNumber(47798); //changing PlateNumber value using setPlateNumber`<br/>
&emsp;`echo "Plate number: " . $obj1->getPlateNumber(); //accessing plateNumber by calling getPlateNumber method`<br/>
&emsp;`echo "\n";`<br/>
&emsp;`$obj2 = new Car("Mercedes", 89976);`<br/>
&emsp;`//uncomment the line below and try running the code`<br/>
&emsp;`//you will get an error as you cannot directly access a private member outside of the class it is declared in`<br/>
&emsp;`//echo $obj2->plateNumber;`<br/>
`?>`<br/><br/>

> By using the get and set functions we were able to access the values of the private members.

<br/>

## Protected
- By Declaring a method or a property as protected allows the method or property to be accessed by:
    - the class that declared it
    - the classes that inherits from the declared class
> Note: This does not allow external objects, classes, or code outside the class hiearachy to access these methods and properties.

- Example: <br>
`<?php`<br>
&emsp;`class Car`<br>
&emsp;`{`<br>
&emsp;&emsp;    `public $name = " ";`<br>
&emsp;&emsp;    `protected $power = 2500;`<br>
&emsp;&emsp;    `public function display()`<br>
&emsp;&emsp;    `{`<br>
&emsp;&emsp;&emsp;        `echo "Name: $this->name" . "\n";`<br>
&emsp;&emsp;    `}`<br>
&emsp;&emsp;    `public function __construct($name)`<br>
&emsp;&emsp;    `{`<br>
&emsp;&emsp;&emsp;       `$this->name = $name;`<br>
&emsp;&emsp;    `}`<br>
&emsp;`}`<br>
&emsp;`//Code`<br>
&emsp;`$obj = new Car("Blue");`<br>
&emsp;`echo $obj->display();`<br>
&emsp;`echo $obj->power; //comment out this line to prevent an error`<br>
`?>`<br><br>

|Modifier|Class|Subclass|World|
|--------|-----|--------|-----|
|Private|✔|❌|❌|
