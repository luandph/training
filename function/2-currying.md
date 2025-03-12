### 1. Currency Formatter

You need to format currency amounts for different locales.

1. Create a function `createCurrencyFormatter(locale, currency)` that returns another function that takes an amount and formats it as currency.
2. Create functions `formatUSD`, `formatEUR`, and `formatJPY` from the function above.

```js
const createCurrencyFormatter = (locale, currency) => {
  /* ... */
};

// partially applied functions
const formatUSD = createCurrencyFormatter("en-US", "USD");
const formatEUR = createCurrencyFormatter("de-DE", "EUR");
const formatJPY = createCurrencyFormatter("ja-JP", "JPY");

console.log(formatUSD(1000)); // "$1,000.00"
console.log(formatEUR(1000)); // "1.000,00 €"
console.log(formatJPY(1000)); // "￥1,000"
```

### 2. Logging Utility

Create reusable log functions for different log levels.

```js
const log = (level) => {
  /* ... */
};

// Partially applied functions
const info = log("info");
const warn = log("warn");
const error = log("error");

info("Application started"); // [INFO] Application started
warn("Low disk space"); // [WARN] Low disk space
error("Server is down!"); // [ERROR] Server is down!
```
