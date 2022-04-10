# Students Average Mark
## Problem Statement
- Write a class called student with private member variables:
    - name
    - mark1 and mark2
    - And methods:
        - getMarks($marknumber), a method which should return mark1 if marknumber equals 1 and mark2 otherwise.
        - calcAverage() method should take the two marks entered and return their average.
    - Also define
        - A constructor that takes the three private variables and sets them to given values.

>`<?php`<br>
>`class Student`<br>
>`{`<br>
>` `<br>
>`    //define private variables here`<br>
>`    private $name = "";`<br>
>`    private $mark1 = 0;`<br>
>`    private $mark2 = 0;`<br>
>` `<br>
>`    public function __construct($na, $ma1, $ma2)`<br>
>`    {`<br>
>`        //write definition here`<br>
>`        $this->name = $na;`<br>
>`        $this->mark1 = $ma1;`<br>
>`        $this->mark2 = $ma2;`<br>
>`    }`<br>
>`    public function getMarks($marknumber)`<br>
>`    {`<br>
>`        //write definition here`<br>
>`        //return -14567; //return correct answer here`<br>
>`        if($marknumber === 1) {`<br>
>`            return $this->mark1;`<br>
>`        }`<br>
>`        else {`<br>
>`            return $this->mark2;`<br>
>`        }`<br>
>`        `<br>
>`    }`<br>
>`    public function calcAverage()`<br>
>`    {`<br>
>`        //write definition here`<br>
>`        //return -14567; //return correct answer here`<br>
>`        return ($this->mark1 + $this->mark2)/2;`<br>
>`      ` <br> 
>`    }`<br>
>`}`<br>
>`?>`<br><br>