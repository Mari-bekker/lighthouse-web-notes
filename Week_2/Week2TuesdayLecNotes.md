# Data Types

### Promitive types. 

Let's review the six types of primitives:
-undefined
-null
-boolean
-string
-number
-symbol

Anything not in that list (for example, a Date) is an Object. Objects are not primitive data types.

# Objects

Can use square brackets to access the key.
But also can add dynamic value in the square brackets if it's changes

example:

```javascript
const keyToLookup = 'name';
console.log(instructor[keyToLookup]);

const keyPrefix = 'dynamic'
console.log(instructor[`${keyPrefix}Key`]);

```

### Primitives are Passed as Values

Meaning that if a variable that is string or a number goes into a function, the value of it that was defined outside of a function does not change. 

### Objects are Passed as References

Changes made to the object in the function, make changes to it outside of it as well
so if you want to just use the data of the object without changing, maybe copy the content to a new variable. 

# Looping Objects and Arrays

### For arrays for ... of

```javascript
const destinations = ['Vancouver', 'Calgary', 'Edmonton', 'Saskatoon', 'Regina'];

for (const destination of destinations) {
    console.log("Now arriving", destination);
}
```

### For objects for...in to iterate through keys

```javascript
const instructors = {
  1: {
      id: '1',
      name: 'Ian'
  },
  2: {
      id: '2',
      name: 'Taiwo'
  }
};

for (const key in instructors) {
  // key is variable, so use bracket notation to access the value
  console.log(key, instructors[key])
}

```
