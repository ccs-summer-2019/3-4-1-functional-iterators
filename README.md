## FUNCTIONAL ITERATORS

### forEach()

  * The forEach() method executes a provided function once for each array element.
  * The reason to use forEach is to have side effects for each item in an array.

  **log each item**
```
  [1, 2, 3].forEach(item => console.log(item));
```
  **add something to an array or string for each item**
```
  let copy = [];

  [1, 2, 3].forEach(item => copy.push(item));
```
### map()

  * The map() method creates a new array with the results of calling a provided function on every element in the calling array.
  * The reason to use map is to transform each item in the array and get a new array.
  * Etiquette says that map should never have side effects, though this isn't enforced in any way.
```
  [1, 2, 3].map(num => num * 2);
```
### filter()

  * The filter() method creates a new array with all elements that pass the test implemented by the provided function.
  * The reason to use filter is to get a new array that only contains items that match the criteria you're looking for.
  * The internal function must return true or false.
  * Etiquette says that filter should never have side effects, though this isn't enforced in any way.
```
  ["spray", "limit", "elite", "exuberant", "destruction", "present", "happy"].filter(
    word => word.length > 6
  ); // => ["exuberant", "destruction", "present"]
```
### reduce()

  * The reduce() method applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.
  * The reason to use reduce is to "reduce" an array of values or objects into a single value or object.
  * If no initial value is supplied, the first element in the array will be used.

  **sum with reduce**
```
  [1, 2, 3].reduce((accum, i) => accum + i); // => 6
```
**starting with a preset accumulator**
```
 [1, 2, 3].reduce((accum, i) => accum + i, 2); // => 8
```
