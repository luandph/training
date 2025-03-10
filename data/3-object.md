### Mutate vs Immutate

Given this object

```js
let school = {
  name: "ABC School",
  classes: [
    {
      name: "1A",
      pupils: [
        {
          name: "John",
        },
        {
          name: "Jane",
        },
      ],
    },
  ],
};
```

1. Add pupil named Jack to class 1A.
2. Add class named 1B having pupil named Mary to school.
3. Move Jane to class 1B.
4. Do the above 3 tasks without mutating the object `school`. Create a new object for each task.
