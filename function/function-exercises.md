### 1. Reimplement array methods

Implement these Javascript array methods: `map`, `filter`, `reduce`, `forEach`, `find`, `sort`, `slice`, `splice`, `push`, `pop`, `shift`, `unshift`

**Notes**

- Do not override the method in `Array.prototype`. Instead, create the function having the array as first param. For example, create a function named `myMap` such that `myMap(arr, callback)` behaves the same as `arr.map(callback)`.
- Behaving the same means: taking same params, returning same result, having same mutability/immutability.
- Refer to the docs to find the description of these methods. For example, https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map
- The goal of this exercise is understanding how these methods work behind the scenes.

### 2. Some Lodash functions

Implement these Lodash array functions: `countBy`, `flatten`, `fromPairs`, `keyBy`, `some`, `zip`

**Notes**

- Check Lodash docs for description, for example, https://lodash.com/docs/4.17.15#countBy
- Make use of the built-in array methods.
