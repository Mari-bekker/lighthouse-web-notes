# util 
This was used to display the inner object content. 

### need to add it to the code like so: 
 const inspect = require('util').inspect;

I used it here:

```javascript 
const assertObjectsEqual = function(actual, expected) {
  const inspect = require('util').inspect;
  let compare = eqObjects(actual, expected);
  
  if (compare === true) {
    console.log(`✅✅✅ Assertion Passed: ${inspect(actual)} === ${inspect(expected)}`);
  } else {
    console.log(`🛑🛑🛑 Assertion Failed: ${inspect(actual)} !== ${inspect(expected)}`);
  }
};
```
# For Each loop notes: 

Example of correct format: 

```javascript
forEach(function(element) { /* ... */ })
forEach(function(element, index)

```

Basically, don't close barackets after the element , index, you need to add a function
basically code that executes for each of the items. And after that can close the code with round bracket. 

Example from my code:

```javascript
const findWaldo = function(names, found) {
  names.forEach(function(element, index) {
    if (element === "Waldo") {
      found(index);   // execute callback
    }
  }); 
}

const actionWhenFound = function(index) {
  console.log(`Found Waldo at index:${index} !`);
}

findWaldo(["Alice", "Bob", "Waldo", "Winston"], actionWhenFound);
```

### NOTE about anynymous functions: 

// Instead of naming the function and making it a separate thing. just pass the function like a parameter
// and then put all what the function is doing inside the curely braces like a normal function.

```javascript
findWaldo(["Alice", "Bob", "Waldo", "Winston"], function(index) {
  console.log("Waldo is located at:", index);
});
```

# Notes about filtering function. 
My own example: 

```javascript
const grades = [73, 69, 3, 100, 50, 70, 69, 88, 95, 77, 35];

const passingGrades = grades.filter((num) => {
  return (num >= 70);
});

console.log("The passing grades are:", passingGrades);
```


# Arrow functions: 

x => x * 2
is same as function (x) { return (x * 2); }