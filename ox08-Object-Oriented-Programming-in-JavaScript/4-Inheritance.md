# Inheritance

Inheritance allows one class to inherit properties and methods from another class.

This helps in code reusability and hierarchical structuring of objects.

In JavaScript, inheritance is implemented using the `extends` keyword with ES6 classes.

Inheritance is used when there is a "is-a" relationship (e.g., A Car is a Vehicle, A Dog is an Animal).

Inheritance helps avoid code duplication when multiple classes share common behavior.
```js
class Animal {
  constructor(numLegs, numEyes) {
    this.numLegs = numLegs;
    this.numEyes = numEyes;
  }

  move() {
    console.log(`Animal looking at the road with ${this.numEyes} eyes`);
    console.log(`Animal moving with ${this.numLegs} legs`);
  }

  eat() {
    console.log(`Animal eating for survival`);
  }
}

class Cow extends Animal {
  constructor(numLegs, numEyes, breed, gender) {
    super(numLegs, numEyes); // calls the parent constructor
    this.breed = breed;
    this.gender = gender;
  }

  sound() {
    console.log(`The ${this.gender} ${this.breed} cow is mooing`);
  }
}

const myCow = new Cow(4, 2, "Guernsey", "Male");
myCow.move();
myCow.eat();
myCow.sound();
```
