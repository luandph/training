### 1. filter

Given this array

```js
const array = [
  { name: "Quan" },
  { name: "Son" },
  { name: "Cuong" },
  { name: "Hung" },
];
```

Write function `filter` such that

```js
filter(array, function (e) {
  return e.name.indexOf("u") > -1;
});

// output
[{ name: "Quan" }, { name: "Cuong" }, { name: "Hung" }];
```

```js
filter(array, function (e) {
  return e.name.indexOf("a") > -1;
});

// output
[{ name: "Quan" }];
```

```js
filter(array, function (e) {
  return e.name.indexOf("x") > -1;
});

// output
[];
```

```js
filter(array, function (e) {
  return e.name.length > 4;
});

// output
[{ name: "Cuong" }];
```

**Notes**: Do not use built-in method `filter`.

### 2. remove and without

#### remove

Write function `remove` such that

```js
const quan = { name: "Quan" };

let array = [quan, { name: "Son" }, { name: "Cuong" }, { name: "Hung" }];

remove(quan, array);

// the array now
[{ name: "Son" }, { name: "Cuong" }, { name: "Hung" }];
```

#### without

Write function `without` such that

```js
const array = [{ name: "Quan" };, { name: "Son" }, { name: "Cuong" }, { name: "Hung" }];

without(array, function( e ) {
	return e.name == "Quan";
});

// output
[
    {name: "Son"},
    {name: "Cuong"},
    {name: "Hung"}
]
```

**Notes**: `remove` modifies the array by removing the targeted element. `without` do not modify the array, instead create a new array, with all elements in it without the one filtered by the given function.

### 3. merge

Write function `merge` such that

```js
const o1 = { name: "Quan" };
const o2 = { age: 23 };

merge(o1, o2)
// output
{ name: "Quan", age: 23}

merge({ name: "Quan", age: 23 }, { age: 25 });
// output
{ name: "Quan", age: 25}

```

**Notes:** Do not use built-in function `assign`.

### 4. addToListMap

Write function `addToListMap` such that:

```js
let listMap = {
	"Hoa": [
		"Le Thi Hoa",
		"Mai Hoa"
	],
	"Tham": [
		"Hong Tham",
		"Xuan Tham"
	]
};

addToListMap("Hoa", "Xuan Hoa", listMap);
// listMap now
{
	"Hoa": [
		"Le Thi Hoa",
		"Mai Hoa",
		"Xuan Hoa"
	],
	"Tham": [
		"Hong Tham",
		"Xuan Tham"
	]
};

addToListMap("Son", "Anh Son", listMap);
// listMap now
{
	"Hoa": [
		"Le Thi Hoa",
		"Mai Hoa",
		"Xuan Hoa"
	],
	"Tham": [
		"Hong Tham",
		"Xuan Tham"
	],
	"Son": [
		"Anh Son"
	]
};
```

### 5. clone

Write function `clone` such that

```js
const person = {
  name: "Tung",
  age: 12,
  address: {
    street: "Le Trong Tan",
    city: "Ha Noi",
  },
};

const hieu = clone(person);
// then
hieu = {
  name: "Tung",
  age: 12,
  address: {
    street: "Le Trong Tan",
    city: "Ha Noi",
  },
};

hieu.name = "Hieu";
hieu.age = 25;
// then
hieu = {
  name: "Hieu",
  age: 25,
  address: {
    street: "Le Trong Tan",
    city: "Ha Noi",
  },
};
// person is unchanged
person = {
  name: "Tung",
  age: 12,
  address: {
    street: "Le Trong Tan",
    city: "Ha Noi",
  },
};

hieu.address.street = "Ba Trieu";
// then
hieu = {
  name: "Hieu",
  age: 25,
  address: {
    street: "Ba Trieu",
    city: "Ha Noi",
  },
};
// person is unchanged
person = {
  name: "Tung",
  age: 12,
  address: {
    street: "Le Trong Tan",
    city: "Ha Noi",
  },
};
```

### 6. sort

Write function `sortByDistance` such that

```js
const array = [3, 7, 23, 1, 5];

sortByDistance(array, 5);
// output
[5, 3, 7, 1, 23];
```

Write function "sort" such that:

```js
const array = [
  { name: "Quan", age: 35 },
  { name: "Luan", age: 24 },
  { name: "Hoa", age: 28 },
];

sort(array, (person) => person.name);
// output
[
  { name: "Hoa", age: 28 },
  { name: "Luan", age: 24 },
  { name: "Quan", age: 35 },
];
```

**Notes:** Can use javascript "sort" function

### 7. deepEqual

Write function `deepEqual` to check if 2 objects are deeply equal.

### 8. getPathData & setPathData

Given the object

```js
const obj = {
  "name": "Luan",
  "address": {
    "line1": "Danang",
  },
};
```

Write function `getPathData` such that

```js
getPathData(obj, ["name"]); // "Luan"
getPathData(obj, ["address", "line1"]); // "Danang"
getPathData(obj, ["age"]); // undefined
```

Write function `setPathData` such that

```js
setPathData(obj, ["name"], "Son");
// return new object
{
  "name": "Son",
  "address": {
    "line1": "Danang",
  },
}
// and the old object obj is unchanged.
```
