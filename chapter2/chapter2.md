# Review of Important JavaScript OOP Concepts

## JavaScript Objects

Three ways to create objects:
- Using native object type constructor
- Using object literal notation
- Using constructor functions

### Object type constructors

- Create object using instance of Object type

```javascript
var myObj = new Object();

myObj.value = "my first value";
myObj.method = function() {
  return this.value;
};

console.log(myObjmethod());
```

### Object literal notation (Simgleton)

```javascript
var MyFirstObj = {
  myFirstValue: 2,
  mySecondValue: 5,

  addValues: function() {
    return this.myFirstValue + this.mySecondValue;
  }
};

console.log(MyFirstObj.addVAlues());
```

## Function objects

- Functions are first class objects

### Functions as object constructors (classes)

```javascript
function MyObjDefinition() {
  var myFirstValue = 2;
  var mySecondValue = 5;

  this.addValues = function() {
    return myFirstValue + mySecondValeu;
  };
}

var myFirstObj = new MyObjDefinition();

console.log(myFirstObj.addValues());
```

### Function as static objects

```javascript
// defining an objnect
function MyObjDefinition() {
  MyObjDefinition.myFirstValue = 2;MyObjDefinition.mySecondValue = 5;
}

// adding a property to the object
MyObjDefinition.addValues = function() {
  return this.myFirstValue + this.mySecondValue;
};

// initializing the object by calling it as a function
MyObjDefinition();

console.log(MyObjDefinition.addValues()); // Displays 7

var anotherObj = new MyObjDefinition();
anotherObj.addValues(); // error
```

## Object literal notation versus function objects

