# Object keys: 

The correct formatting is: 

Object.keys(nameOfmyObject);

What this does is return an array of the keys. 
so if my object was {a: 1, b:2, c:3} it will make an array like [a, b, c].
And since it's an array we can iterate over it. 

# Using incluse to iterate over array: 

### The correct formatting of include is: arrayName.includes(value)'

### This will check if an array will contain the value, effectivelly replacing a loop!
So you in essence can iterate through an array full of other arrays, and not have to have a second loop going. 


```javascript
const raisinAlarmArray = function(cookies) {
  // create an empty array result
  // iterate through the array cookies
  // if the array contains grape, push to result array

  let result = [];
  for (let item of cookies) {
    if (item.includes("🍇")) {
      result.push("Raisin Alert");
    } else {
      result.push("All Good!");
    }
  }
  return result;
};

console.log(raisinAlarmArray(
  [
    ["🍫", "🍫", "🍇", "🍫"],
    ["🍫", "🍇", "🍫", "🍫", "🍇"],
    ["🍫", "🍫", "🍫"]
  ]
));
```
# Remembering to prioritize false statements

Instead of going into nested if then statements, consider that if we encounter false we can leave the whole function.

so one approach can adopt is always return true, and then figure out all the excpetions and write them. 