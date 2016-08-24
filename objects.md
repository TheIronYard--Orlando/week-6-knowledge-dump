An object is a collection of properties, and a property is an association between a name (or key) and a value. Objects in javascript can be associated with objects in real life. Envision your car, car will have multiple properties like make, model, and color.
Example:
var myCar = {make: "Toyota", model:"Camry", color: "silver"}
myCar.make (this will return "Toyota")

Users may access the values using dot or bracket notitation.
myCar.make === myCar["make"] (returns true)

Object-oriented programming (OOP) is a programming model that uses abstraction to create models based on the real world. OOP envisions software as a collection of cooperating objects rather than a collection of functions or a list of commands. OOP allows for the user to develop more simple code, in addition make it more easy to understand later on.

Example:
var myCarConstructor = function(make, model, year) {
 this.make = make;
 this.model = model;
 this.year = year;
}

var edsCar = new myCarConstructor("Toyota", "Camry", 2007);
var briansCar = new myCarConstructor("Mercedez", "S12", 2016);

edsCar.make; (returns "Toyota")
briansCar.model; (returns "S12")

In JavaScript <em>this</em> always refers to the “owner” of the function the user executing, or rather, to the object that a function is a method of. The can use this.key to return the value of that property.

Calling <em>this</em> outside of any functions on a webpage will actually return the Window object.
