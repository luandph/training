### 1. Currency Formatter

You need to format currency amounts for different locales.

Write function `createCurrencyFormatter` that returns another function that takes an amount and formats it as currency.

```js
const createCurrencyFormatter = (locale, currency) => {
  /* ... */
};

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

const info = log("info");
const warn = log("warn");
const error = log("error");

info("Application started"); // [INFO] Application started
warn("Low disk space"); // [WARN] Low disk space
error("Server is down!"); // [ERROR] Server is down!
```

### 3. Rate Limiter

You need a rate limiter for an API to restrict the number of requests per user.

Write function `createRateLimiter` that returns another function taking a `userId`. This tracks how many requests a userID makes within the time window. If they exceed the max request number, return "Rate limit exceeded"; else returns "Request allowed".

```js
const createRateLimiter = (maxRequests, windowMs) => {
  /* ... */
};

// Partially applied function
const apiLimiter = createRateLimiter(3, 10 * 1000); // Max 3 requests per 10 sec

console.log(apiLimiter("user123")); // "Request allowed"
console.log(apiLimiter("user123")); // "Request allowed"
console.log(apiLimiter("user123")); // "Request allowed"
console.log(apiLimiter("user123")); // "Rate limit exceeded"
```
