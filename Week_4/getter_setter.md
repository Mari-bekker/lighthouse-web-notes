Super:

Using super allows us to access the superclass

Example: 

class Mentor extends Person {
  // Mentor bios need to include a bit more info
  bio() {
    return `I'm a mentor at Lighthouse Labs. ${super.bio()}`;
  }
}
Getters and Setters: 
- special methods that are used to get the value of a property or set the value of a property. 

why do we use it instead of calling something directly like pizza.size?

1. Validating data before assignning it to a property
2. Computing a value on the fly instead of simply pulling it out of a property. 