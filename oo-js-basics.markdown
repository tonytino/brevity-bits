# Basics of OO-JavaScript

## Object Literals

*Ideal for creating one-off objects.*

Example:

```javascript

var dice = {
  value: 0,
  sides: 6,
  baseColor: "white",
  dotColor: "black",
  roll: function() {
    this.value = Math.floor(Math.random() * (this.sides)) + 1;
  }
}

dice.value // 0
dice.roll() // will return a random number between 1 - 6, which dice.value will be set equal to (e.g. 4)
dice.value // based on the previous line, would return 4

```

## Constructors and Prototypes

Constructors will be the go-to methodology for:

- Defining how an object type should exist (what characteristics and functionality it should have)
- Having the ability to create multiple instances of the same object type (copies structure)
- Having similar objects with different states (methods and properties will be the same, values may be different)

*It is conventional to capitalize the first letter of the name of your constructor.*

```javascript

// defining your constructor

function Dice(sides) {
  this.value = 0;
  this.sides = sides;
  this.baseColor = "white";
  this.dotColor = "black";
}

// then, create all your methods, which will be available in each instance of your object type
// we do this outside of the constructor so that all instances reference the same function, rather than consuming extra memory by creating the same function multiple times

Dice.prototype.roll = function () {
  this.value = Math.floor(Math.random() * this.sides) + 1;
}

// creating an instance of your constructor

var myDice = new Dice(5);

myDice.value // 0
myDice.roll() // will return a random number between 1 - 6, which myDice.value will be set equal to (e.g. 4)
myDice.value // based on the previous line, would return 4

```

## Prototype Chaining (Prototypal Inheritance)

Prototype chaining allows you to extend the properties and functionality of a constructor without making such properties and functionality exclusive to such constructor. In other words, if some properties and functionality are appropriate for similar objects (e.g. trucks and cars, very similar yet distinctly different), you can separate the overlapping properties and functions into an additional constructor, which can be inherited by other constructors.

```javascript

function RoadVehicle(engineSize, tireCount) {
  this.engineSize = engineSize;
  this.tireCount = tireCount;
}

function Truck(engineSize, tireCount, bedSize) {
  RoadVehicle.call(this, engineSize, tireCount); // this line calls on the properties of RoadVehicle for the purpose of adding these properties to our truck instance. "this" references the new truck instance. note that we don't create a "new" instance of RoadVehicle, we just call on its properties to extend the properties of our truck instance.
  this.bedSize = bedSize;
  this.towing = false;
}

Truck.prototype = Object.create(RoadVehicle.prototype); // this is what causes Truck to inherit from RoadVehicle

Truck.prototype.tow = function () {
  this.towing = true;
}

```