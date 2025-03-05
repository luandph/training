### 1. Array methods

Implement these Javascript array methods: `map`, `filter`, `reduce`, `forEach`, `find`, `sort`, `slice`, `splice`, `push`, `pop`, `shift`, `unshift`

**Notes**

- Do not override the method in `Array.prototype`. Instead, create the function having the array as first param. For example, create a function named `myMap` such that `myMap(arr, callback)` behaves the same as `arr.map(callback)`.
- Behaving the same means: taking same params, returning same result, having same mutability/immutability.
- Refer to the docs to find the description of these methods. For example, https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map
- The goal of this exercise is understanding how these methods work behind the scenes.

### 2. Array methods practice

Given this data

```js
const characters = [
  {
    name: "Luke Skywalker",
    height: "172",
    mass: "77",
    eyeColor: "blue",
    gender: "male",
  },
  {
    name: "Darth Vader",
    height: "202",
    mass: "136",
    eyeColor: "yellow",
    gender: "male",
  },
  {
    name: "Leia Organa",
    height: "150",
    mass: "49",
    eyeColor: "brown",
    gender: "female",
  },
  {
    name: "Anakin Skywalker",
    height: "188",
    mass: "84",
    eyeColor: "blue",
    gender: "male",
  },
];
```

##### MAP

1. Get an array of all names
2. Get an array of all heights
3. Get an array of objects with just name and height properties
4. Get an array of all first names

##### REDUCE

1. Get the total mass of all characters
2. Get the total height of all characters
3. Get the total number of characters in all the character names
4. Get the total number of characters by eye color (hint. a map of eye color to count)

##### FILTER

1. Get characters with mass greater than 100
2. Get characters with height less than 200
3. Get all male characters
4. Get all female characters

##### SORT

1. Sort by name
2. Sort by mass
3. Sort by height
4. Sort by gender

##### EVERY

1. Does every character have blue eyes?
2. Does every character have mass more than 40?
3. Is every character shorter than 200?
4. Is every character male?

##### SOME

1. Is there at least one male character?
2. Is there at least one character with blue eyes?
3. Is there at least one character taller than 200?
4. Is there at least one character that has mass less than 50?

### 3. Some Lodash functions

Implement these Lodash array functions: `countBy`, `flatten`, `fromPairs`, `keyBy`, `some`, `zip`

**Notes**

- Check Lodash docs for description, for example, https://lodash.com/docs/4.17.15#countBy
- Make use of the built-in array methods.
