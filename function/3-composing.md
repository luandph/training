### 1. Format and Display User Information

You have user data coming from an API, and you need to format and display it properly. The steps are

1. Extract and return the full name from a user object.
2. Convert the name to uppercase.
3. Add title "Mr./Ms.", or return "Unknown User" if the name is empty.

```js
// Write these functions
const getFullName = (user) => {
  /* ... */
};
const toUpperCase = (str) => {
  /* ... */
};
const addTitle = (name) => {
  /* ... */
};

// composition of the above functions
const formatUser = (user) => {
  /* ... */
};

console.log(formatUser({ firstName: "John", lastName: "Doe" })); // "Mr./Ms. JOHN DOE"
console.log(formatUser({ firstName: "Jane" })); // "Mr./Ms. JANE"
console.log(formatUser({})); // "Unknown User"
```

**Hints:** for the composition, use the function `pipe` that use wrote in the currying section.

### 2. Sanitize User Input

You need to sanitize a user input. The steps are

1. Trim whitespace from input.
2. Convert input to lowercase.
3. Remove special characters (keep only letters and numbers).
4. Limit the input to 20 characters.

```js
// Write these functions
const trim = (str) => {
  /* ... */
};
const toLowerCase = (str) => {
  /* ... */
};
const removeSpecialChars = (str) => {
  /* ... */
};
const limitLength = (max) => (str) => {
  /* ... */
};

// composition of the above functions
const sanitizeInput = (str) => {
  /* ... */
};

console.log(sanitizeInput("   Hello@WORLD!!! Welcome to JavaScript.  "));
// Expected output: "hello world welcome"
```

### 3. Display Prices

You need to display some prices. For a price, the steps are

1. Convert from cents to dollars.
2. Apply a given discount to the price.
3. Format the price as a string with $ and two decimal places. If price is zero, show "Free".

```js
// Write these functions
const toDollars = (priceInCents) => {
  /* ... */
};
const applyDiscount = (discount) => (price) => {
  /* ... */
};
const formatPrice = (price) => {
  /* ... */
};

// composition of the above functions
const processPrices = (prices, discount) => {
  /* ... */
};

const prices = [0, 500, 1500, 0, 20000]; // cents
console.log(processPrices(prices, 0.1)); // Expected output: ["Free", "$4.50", "$13.50", "Free", "$180.00"]
```

### 4. Transform API Response

You need to process data returned from an API into an array of active users' names. The steps are

1. Extract data from the API response.
2. Filter only active users.
3. Get an array of user names.
4. Sort the names alphabetically.

```js
// Write these functions
const extractData = (res) => {
  /* ... */
};
const filterActive = (users) => {
  /* ... */
};
const mapUserNames = (users) => {
  /* ... */
};
const sortNames = (names) => {
  /* ... */
};

// composition of the above functions
const processUsers = (res) => {
  /* ... */
};

const apiResponse = {
  data: [
    { name: "Charlie", active: true },
    { name: "Alice", active: true },
    { name: "Bob", active: false },
  ],
};

console.log(processUsers(apiResponse)); // Expected output: ["Alice", "Charlie"]
```

### 5. Generate SEO-Friendly URLs

You need to turn a title into a slug. The steps are

1. Remove punctuation.
2. Convert to kebab-case (lowercase words separated by -).
3. Limit the length to 50 characters, but ensure that words are not cut off.

```js
// Write these functions
const removePunctuation = (str) => {
  /* ... */
};
const toKebabCase = (str) => {
  /* ... */
};
const limitLengthSafely = (max) => (str) => {
  /* ... */
};

const createSlugGenerator = ({ maxLength }) => {
  // composition of the above functions
  return (title) => {
    /* ... */
  };
};

const generateSlug = createSlugGenerator({ maxLength: 50 });

console.log(
  generateSlug(
    "10 Tips to Write Great JavaScript Code for Beginners and Experts!",
  ),
);
// Expected output: "10-tips-to-write-great-javascript-code"
```
